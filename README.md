# 80k-SHA256-Powershell-check
Utilizing 80k+ of SHA256 identifiers, Checks a host machine against it for malware
First, you will need to obtain a database of known malware hashes. You can find several free databases online, such as the VirusTotal database or the National Software Reference Library (NSRL) database.

Next, you will need to download the malware hash database and import it into a PowerShell script. You can do this by downloading the database as a CSV file and using the Import-Csv cmdlet to import it into a PowerShell object.

Once you have imported the database into your script, you can use a loop to iterate through each file on the system and calculate its hash. You can use the Get-FileHash cmdlet to calculate the hash of a file.

After calculating the hash of a file, you can use the Where-Object cmdlet to search the database for the hash. If the hash is found in the database, it indicates that the file is likely malware. You can then display a message or take other actions as necessary.

This script will search the specified root directory (in this case, the "C:" directory) and its subdirectories for files. It will then calculate the hash of each file and search the database for the hash. If the hash is found in the database, it will display a message indicating that malware was detected.

You can modify the script to start the search from a different root directory or to use a different algorithm for calculating the hashes by changing the values of the $root and -Algorithm parameters. You can also modify the script to perform other actions when malware is detected, such as deleting the file or quarantining it.
