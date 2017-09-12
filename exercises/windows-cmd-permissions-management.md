# Windows cmd.exe Permissions Management Challenge

1. At the command line, take the following steps:

  - Create a directory called `C:\StrangerThings`
  - Change into that directory
  - Create the following directories within the `StrangerThings` directory, and use `icacls` to set the following permissions for **your** user account

    - Name:
      - Eleven
    - Permissions:
      - Full access
    - Name:
      - Mike
    - Permissions:
      - Read and execute access
    - Name:
      - Will
    - Permissions:
      - Read only access
    - Name:
      - Dustin
    - Permissions:
      - Read and execute access
      - Modify access
      - Delete access
    - Name:
      - Lucas
    - Permissions:
      - Read and execute access
      - Modify access

1. Add a `secret.txt` file with a random string to each of the above directories that you must keep safe from the `Demogorgon` and other `Demons`

1. Using the `net` command, add another user to your system named `Demogorgon`

1. Using the `net` command, create a group called `Demons`

1. Using the `net` command, add `Demogorgon` to the `Demons` group

1. Are the kids now safe from the `Demogorgon`?
  - Show an instructor how you prove this

1. Using the `net` command, create the following users
  - Eleven
  - Mike
  - Will
  - Lucas
  - Dustin

1. Using the `net` command, create a new group called `Heros`

1. Add all of the kids into the `Heros` group

1. Using the `icacls` command add `Full access` permissions to the `Heros` group on `C:\StrangerThings` directory

1. Using the `icacls` command, add a command to protect the kids in the `C:\StrangerThings` directory from the `Demogorgon`

1. Would the kids now be safe from other `Demons` also?
  - Show an instructor how you intend to keep the kids safe from all other `Demons`

1. The kids need to be able to share secrets with each other, but make sure that their secrets cannot be changed by anyone else, not even each other.

1. Using the `icacls` command, add the proper permissions to each secret file so that the other kids can read their secrets, but only the owner can change the secret
  - Show an instructor that your solution works

1. Using the `net` command remove all created users and groups


**HINT:** If you don't want to log in and out of different User accounts you can use the following commands to launch programs in your current session as another user from Powershell:

`runas /user:Username powershell.exe`
