# TridentBackup
Backup of Trident config files

Uses master branch for Raspberry Pi git CLI

Copies all of klipper_config directory.

## Next backups
Next time you want to backup your printer settings, you need to SSH into your pi and type:

  ```
  cd ~/klipper_config/
  git add .
  git commit -m "backup"
  git push -u origin master
  ```

Copied!
Enter your GitHub credentials and you're done!

## Restore with git
If you need to completely restore your settings in the already existing local folder: 

  ```
  cd ~/klipper_config/
  git fetch -all
  git reset --hard origin/master
  ```

**WARNING! This will delete all your settings in your printer folder and replace them with your backup. You will lose any change that was not backed up!!**

Source: https://lazarofilm.gitbook.io/3d-printing/creating-a-github-backup-for-klipper!
