echo "what command do u want to execute-SCP or SSH"
while :
do
read INPUT_STRING
case $INPUT_STRING in
        SCP)
                echo "u have selected SCP"



               echo "please provide the username and IP"
                read a b
                scp -r $a@$b /home/$a
                ;;
        SSH)
                echo "U have selected SSH"
                echo "please provide the username and IP number of client"
                read c d
                ssh $c@$d whoami
                ;;



       *)
                echo "Not a valid argument"
                echo
esac
