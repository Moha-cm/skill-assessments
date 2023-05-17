Q1: What is your home directory?
A: /home/ubuntu

Q2: What is the output of this command?
A:  hello_world.txt

Q3: What is the output of each ls command?
A:  my_folder  -->  has return empty list
     my_folder --> has return "hello_world.txt" file

Q4: What is the output of each?
A:  my_folder --> return empty list (because  of no files or folder)
     my_fodler2 --> return empty list ( because of no files or folder)
     my_folder3 --> return the file "hello_world.txt "  file

Q5: What editor did you use and what was the command to save your file changes?
A:  I have used nano text editor
    steps used :
        1.nano  hello_word.txt
        2.edit the world to linux
        3.ctl + x
        4.then  "Y" key to save the changes to save

Q6: What is the error?
A:  No supported authentication methods available (server sent: publickey)

Q7: What was the solution?
A:  First create the user and then add the SSH public key that allows the user to connect to and log into the instance
        Steps:
        1.Create a new key pair  using " ssh-keygen"  local terminal using Mobaxterm. It create a publica nd private key named  "id_rsa", "id_rsa.pub"
        2.Connect to the instance
        3.Switch to sudouser by command " su - sudouser". Then enetr the password.
        4.The promt changes from ubuntu to sudouser to indicate that you have switched the shell session to the sudouser
        5.Add the SSH public key to the sudouser. First create a directory in the user's home directory for SSH key file, then create the key file and finally paste the public key into the key file by the following commands
        6.Create the directory  and  change its file permissions
                                   --> mkdir .ssh
                                   --> chmod 700 .ssh
        7.Create file named authorized_keys in .ssh directory and change its file permissions to 600
                                           --> cd .ssh
                                           ---> touch authorized_keys
                                            --> chmod authorized_keys
        8.open the authorized_keys file by text editor
                                             --> nano authorized_keys
        9.copy the text from public key and paste in authorized_keys and save the changes 
        10.then, connect with the command  ssh -v  sudouser@18.212.168.185

Q8: what does the sudo "docker run" part of the command do? and what does the salmon swim part of the command do?
A:       docker run --> the command is used to create and start a new Docker container from an image.
         salmon swim  -->   passed as an argument to the container being run

Q9: What is the output of this command?
A:      serveruser is not in the sudoers file.  This incident will be reported.

Q10: What is the output of flask --version?
A:         Python 3.9.16
           Flask 2.2.3
           Werkzeug 2.2.3

Q11: What is the output of mamba -V?
A:        conda 23.1.0
          mamba activate py27

Q12: What is the output of which python?
A:        Python 2.7.15

Q13: What is the output of which python now?
A:            Python 3.9.16

Q14: What is the output of salmon -h?
A:   salmon v1.10.1
      Usage:  salmon -h|--help or
            salmon -v|--version or
           salmon -c|--cite or
           salmon [--no-version-check] <COMMAND> [-h | options]
     Commands:
           index      : create a salmon index
          quant      : quantify a sample
          alevin     : single cell analysis
          swim       : perform super-secret operation
          quantmerge : merge multiple quantifications into a single file

Q15: What does the -o athal.fa.gz part of the command do?
A:      This command  specify the output file of the dowloading file in the name of  athal.fa.gz

Q16: What is a .gz file?
A:     ".gz" indicates the compressed version of the original file
        ".gz" means gzip hepls to reduces the size of the file without loseing the file contents

Q17: What does the zcat command do?
A:      List the contents of the compressed file without unzipping

Q18: what does the head command do?
A:  It helps to view the first few lines of  the file. Helps in quicky to view the beganing of the file.

Q19: what does the number 100 signify in the command?
A:   It is the argument provided to display 100 lines

Q20: What is | doing? -- Hint using | in Linux is called "piping"
A:   It takes the  output of zcat and pass into  as input in the head command.
     Redirect the output of one commad to input of another command.

Q21: What is a .fa file? What is this file format used for?
A:   ".fa" indicates the fasta file. It  a text based format  used in storing DNA, RNA, Protein sequences .

Q22: What format are the downloaded sequencing reads in?
A:    The dowloaded sequence reads are in  -->   .sra format

Q23: What is the total size of the disk?
A:   7.6G

Q24: How much space is remaining on the disk?
A:  2.1G

Q25: What went wrong?
A:   Storage exhausted while writing file within file system module

Q26: What was your solution?
A:   compressing the file by gzip   with command
     fastq-dump --gzip --split-3 SRR074122