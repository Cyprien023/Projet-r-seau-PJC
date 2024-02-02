version 12.4
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname AS8
!
boot-start-marker
boot-end-marker
!
enable secret 5 $1$7qV7$64t1pXlK/NDJ7S6sOrCzT0
!
no aaa new-model
memory-size iomem 5
ip cef
!
!
no ip dhcp use vrf connected
!
ip dhcp pool LAN4_2
   network 192.168.6.0 255.255.255.0
   default-router 192.168.6.254 
!
!
!
multilink bundle-name authenticated
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!         
!
!
archive
 log config
  hidekeys
! 
!
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 192.168.4.1 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/1
 ip address 192.168.6.254 255.255.255.0
 duplex auto
 speed auto
!         
router ospf 1
 log-adjacency-changes
 network 192.168.4.1 0.0.0.0 area 0
!
ip forward-protocol nd
!
!
ip http server
no ip http secure-server
!
!
!
!
!
!
!
control-plane
!
!
!
!
!
!         
!
!
!
!
line con 0
line aux 0
line vty 0 4
 login
!
!
end