# Exam_2420


/* Part 1 */

code{

	sudo apt update 
	sudo apt upgrade


}
![Screenshot 2022-12-08 123510](https://user-images.githubusercontent.com/91351142/206568733-79b0d294-4bee-4523-b253-79c453104b05.png)


/* Part 2 */


I used the command x to delete the words or characters that needs changes
I used cw to change the word and press Escape to apply the necessary changes
h : was used to go left
l : to go right
j : to go down
k : to go up


/* Part 3 */

Print logs for the current boot: journalctl -b

Priority warning for logs: journalctl -b -p warning

Output in a nice pretty JSON: journalctl -b -p warning --output json-pretty


/* Part 4 */


code {

#!/bin/bash

# Search the /etc/passwd file for all users with UID between 1000 and 5000
users=$(grep -E ":([1-4][0-9]{3}):" /etc/passwd)

# Cycle through users
for user in $users; do
  # Extract the user name, UID and login shell
  name=$(echo $user | cut -d: -f1)
  uid=$(echo $user | cut -d: -f3)
  shell=$(echo $user | cut -d: -f7)

  # Print the user name, UID and login shell
  printf "Username: %s\nUID: %s\nLogin Shell: %s\n\n" "$name" "$uid" "$shell"
# Print all currently logged in users
loggedin=$(w | tail -n +3 | awk '{print $1}')

# Cycle through logged in users
for user in $loggedin; do
  # Print the user name# Print all currently logged in users
loggedin=$(w | tail -n +3 | awk '{print $1}')

# Cycle through logged in users
for user in $loggedin; do
  # Print the user name
  printf "Logged in user: %s\n
  printf "Logged in user: %s\n
done

}



/* Part 5 */

code {
Write a service file that runs script from part 4

[Unit]
Description=Part 4 Script

[Service]
Type=simple
ExecStart=/usr/bin/env \\wsl.localhost\Ubuntu\home\stephen\Exam_2420\part4script
Restart=on-failure

[Install]
WantedBy=multi-user.target
~                                                                           ~                                                                           ~                                                                           ~
}

/* Part 6 */





