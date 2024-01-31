-R2_1 : 
Using 706 out of 57336 bytes
!
version 12.4
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption

hostname Router

boot-start-marker
boot-end-marker

no aaa new-model
memory-size iomem 5
ip cef

multilink bundle-name authenticated
archive   
 log config
  hidekeys
    
interface FastEthernet0/0
 ip address 169.255.12.254 255.255.255.0
 duplex auto
 speed auto
    
interface FastEthernet0/1
 ip address 192.168.2.254 255.255.255.0
 duplex auto
 speed auto
       
ip forward-protocol nd
     
ip http server
no ip http secure-server
   
control-plane     
line con 0
line aux 0
line vty 0 4
end       







R3_1 : 
Using 706 out of 57336 bytes

version 12.4
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption

hostname Router

boot-start-marker
boot-end-marker

no aaa new-model
memory-size iomem 5
ip cef

multilink bundle-name authenticated
archive   
 log config
  hidekeys
        
interface FastEthernet0/0
 ip address 169.255.13.254 255.255.255.0
 duplex auto
 speed auto
    
interface FastEthernet0/1
 ip address 192.168.3.254 255.255.255.0
 duplex auto
 speed auto
       
ip forward-protocol nd
     
ip http server
no ip http secure-server
       
control-plane
   
line con 0
line aux 0
line vty 0 4
    
end       





R1_4 : 
Using 795 out of 57336 bytes

version 12.4
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption

hostname Router

boot-start-marker
boot-end-marker

no aaa new-model
memory-size iomem 5
ip cef

multilink bundle-name authenticated
archive   
 log config
  hidekeys
     
interface FastEthernet0/0
 ip address 169.255.13.1 255.255.255.0
 duplex auto
 speed auto
     
interface FastEthernet0/1
 ip address 169.255.12.1 255.255.255.0
 duplex auto
 speed auto
 
interface FastEthernet1/0
 ip address 192.168.10.1 255.255.255.0
 duplex auto
 speed auto
   
ip forward-protocol nd
   
ip http server
no ip http secure-server
control-plane

line con 0
line aux 0
line vty 0 4
       
end




