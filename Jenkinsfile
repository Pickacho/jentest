node{
    def server = Artifactory.server 'art1'
    
    def uploadSpec = """{
  "files": [
    {
      "pattern": "/tmp/file.txt",
      "target": "generic-local/"
    }
 ]
}"""
sh label: '', script: 'echo $HOSTNAME'
sh label: '', script: 'ifconfig |grep inet |grep -v inet6 |grep -v 127.0.0.1'
sh label: '', script: 'scp cloud_user@localhost:/tmp/file1.txt  /tmp/file.txt'
server.upload spec: uploadSpec
}
