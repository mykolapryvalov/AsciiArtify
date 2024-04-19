# Minimum Viable Product (MVP):

### Argo CD Application Setup

![argodemosetup](https://github.com/mykolapryvalov/AsciiArtify/blob/main/doc/img/argodemosetup.gif)

### Testing the AsciiArtify app

forward ports: 

    $ k port-forward -n demo svc/ambassador 8081:80&
    Forwarding from 127.0.0.1:8081 -> 80
    Forwarding from [::1]:8081 -> 80

Check that server answer:

    $ curl localhost:8081
 
Let's check the app's performance:







