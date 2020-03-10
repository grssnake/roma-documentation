sudo apt-get install rabbitmq-server
sudo rabbitmqctl add_user roma FollowTheWhiteRabbit
sudo rabbitmqctl set_user_tags roma administrator
sudo rabbitmqctl set_permissions -p / roma ".*" ".*" ".*"

http://RobotRoma.local:15672/
