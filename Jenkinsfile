pipeline{
agent any
tool{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch:'master'.url:'https://github.com/varshini663/Maveeeen.git'
}
}
stage('Build'){{
steps{
sh'mvn clean install'
}
}
stage('Test'){{
steps{
sh'mvn test'
}
}
stage('Run'){{
steps{
sh'java -jar target/Maveeeen-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo'success'
}
failure{
echo'no'
}
}
}



