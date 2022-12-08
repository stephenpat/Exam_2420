# Exam_2420


/* Part 1 */

code{

	sudo apt update 
	sudo apt upgrade
![Screenshot 2022-12-08 123510](https://user-images.githubusercontent.com/91351142/206576114-61ee18d3-ab15-43b6-ac49-4f4ec6cca770.png)


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
![Screenshot 2022-12-08 124149](https://user-images.githubusercontent.com/91351142/206576030-23a05e31-380a-4506-a322-40be0cedb349.png)


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



![journalctlboot1](https://user-images.githubusercontent.com/91351142/206576140-5a0baeb3-4f58-4736-af3c-1f699ff15c58.png)
![journalctljson](https://user-images.githubusercontent.com/91351142/206576142-ce6bb00a-bedd-4087-9456-13236f35c4ec.png)
![journalctlwarningpriority](https://user-images.githubusercontent.com/91351142/206576144-05000aae-1397-4d79-b710-e46058731ddb.png)
![journatctl warning](https://user-images.githubusercontent.com/91351142/206576145-a4c286a4-d628-4ef8-9095-a4308607c345.png)
![pathservice](https://user-images.githubusercontent.com/91351142/206576146-e9a25cbb-4f93-4526-a8f4-753d298ca2b8.png)
![Screenshot 2022-12-08 123510](https://user-images.githubusercontent.com/91351142/206576147-6bfad5c8-6ab2-4235-91dc-8277f5cac0b7.png)
![Screenshot 2022-12-08 124149](https://user-images.githubusercontent.com/91351142/206576149-fa3daaa3-b11b-4c87-b2b6-9f3479354616.png)
![script](https://user-images.githubusercontent.com/91351142/206576150-6965a215-77e4-4f5c-9c53-a2e091e91b51.png)
![servicefile](https://user-images.githubusercontent.com/91351142/206576151-7ea9e376-1eab-4d3e-ac49-ae6c438743b7.png)
![startservice](https://user-images.githubusercontent.com/91351142/206576152-478820c9-4d48-4bc6-8534-f1f3dda881bc.png)
![systemenable](https://user-images.githubusercontent.com/91351142/206576153-f20dbd81-45fe-4ba7-9fbf-29247d9ae9e5.png)
![journalctlboot](https://user-images.githubusercontent.com/91351142/206576154-48d28904-d8ab-49b3-ba8e-c2ba90713ce2.png)


