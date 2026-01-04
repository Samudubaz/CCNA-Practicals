# Cisco Router and Switch Basic Configuration Notes

---

## 1. Cisco CLI Access Levels

### 1.1 ROMMON Mode
- Used for low-level troubleshooting and password recovery.
- Prompt:
```
rommon>
```

### 1.2 Initial Configuration Dialog
- Appears when a router is started with no configuration.
- Question:
```
Would you like to enter the initial configuration dialog? [yes/no]
```

### 1.3 User EXEC Mode
- Limited monitoring commands only.
- Prompt:
```
Router>
```

### 1.4 Privileged EXEC Mode
- Full access to monitoring and configuration commands.
- Prompt:
```
Router#
```
- Command to enter:
```
Router> enable
```

### 1.5 Global Configuration Mode
- Used to configure the device.
- Prompt:
```
Router(config)#
```
- Command to enter:
```
Router# configure terminal
```

---

## 2. Basic CLI Navigation Commands

| Command | Purpose |
|------|--------|
| enable | Enter Privileged EXEC mode |
| configure terminal | Enter Global Configuration mode |
| exit | Exit current mode |
| ? | Show available commands |

---

## 3. Setting Date and Time (Clock Configuration)

### Commands
```
Router> enable
Router# show clock
Router# clock set 16:09:50 02 December 2023
```
- Used to manually set system date and time.

---

## 4. Changing Device Hostname

### Commands
```
Router# configure terminal
Router(config)# hostname R-01
```
- Sets the router name to **R-01**.

---

## 5. Enable Password Configuration

### 5.1 Configure Enable Password (Plain Text)
```
R-01# configure terminal
R-01(config)# enable password Cisco@SL
```

### 5.2 Remove Enable Password
```
R-01(config)# no enable password
```

---

## 6. Enable Secret Password (Encrypted – Recommended)

### 6.1 Configure Enable Secret
```
R-01# configure terminal
R-01(config)# enable secret Cisco@BAZ
```

### 6.2 Remove Enable Secret
```
R-01(config)# no enable secret
```

---

## 7. Viewing Device Configuration

### Show Running Configuration
```
R-01# show running-config
```
- Displays the current active configuration.

---

## 8. Console Password Configuration

### 8.1 Set Console Password
```
R-01# configure terminal
R-01(config)# line console 0
R-01(config-line)# password Cisco@Console
R-01(config-line)# login
```

### 8.2 Remove Console Password
```
R-01(config)# line console 0
R-01(config-line)# no password
```

---

## 9. Telnet (VTY) Password Configuration

### 9.1 Set Telnet Password
```
R-01(config)# line vty 0
R-01(config-line)# password Cisco@Telnet
R-01(config-line)# login
```

### 9.2 Remove Telnet Password
```
R-01(config)# line vty 0
R-01(config-line)# no password
```

---

## 10. Banner Message Configuration (MOTD)

### Purpose
- Displays a legal/security warning before login.

### Commands
```
R-01(config)# banner motd *
######################################################
This is Secure Area
######################################################
*
```

---

## 11. Encrypting Plain Text Passwords

### Command
```
R-01(config)# service password-encryption
```
- Encrypts console, VTY, and enable passwords.

---

## 12. Interface IP Address Configuration (Router)

### 12.1 GigabitEthernet 0/0/0
```
R-01(config)# interface gigabitethernet 0/0/0
R-01(config-if)# description SW-01-Link
R-01(config-if)# ip address 192.168.1.1 255.255.255.0
R-01(config-if)# no shutdown
```

### 12.2 GigabitEthernet 0/0/1
```
R-01(config)# interface gigabitethernet 0/0/1
R-01(config-if)# description SW-02-Link
R-01(config-if)# ip address 192.168.2.1 255.255.255.0
R-01(config-if)# no shutdown
```

---

## 13. Saving Configuration

### Save Running Configuration to Startup Configuration
```
R-01# copy running-config startup-config
```
- Ensures configuration is retained after reboot.

---

## 14. Switch Management IP Configuration

### VLAN 1 Interface Configuration
```
SW-01(config)# interface vlan 1
SW-01(config-if)# ip address 192.168.1.100 255.255.255.0
SW-01(config-if)# no shutdown
```

### Default Gateway Configuration
```
SW-01(config)# ip default-gateway 192.168.1.1
```

---

## 15. Summary
- Always use **enable secret** instead of enable password.
- Save configuration after changes.
- Use banners for security warnings.
- Assign IP addresses to router interfaces and VLANs correctly for connectivity.
