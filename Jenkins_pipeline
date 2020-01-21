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
sh label: '', script: 'scp cloud_user@34.248.191.20:/tmp/file.txt  /tmp/file.txt'
server.upload spec: uploadSpec
}
