pipeline {
agent {
label {
label "built-in"
customWorkspace "/var/www/html"
}
}
stages {
stage ("one") {
steps { 
sh "sudo yum install httpd -y"
}
}
stage ("two") {
steps {
sh "sudo chmod -R 777 /var/www/html "
sh "sudo service httpd restart"
sh "sudo chkconfig httpd on"
}
}
}
}
