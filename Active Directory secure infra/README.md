# ENTERPRISE ACTIVE DIRECTORY & SECURE INFRASTRUCTURE PLATFORM

- This project simulates a secure enterprise IT infrastructure for an enterprise organization:
  - Centralized identity management
  - Network segmentation (LAN / DMZ / MGMT)
  - Perimeter firewall security
  - VPN remote access
  - IDS monitoring
  - Endpoint hardening
  - Patch management
  - Monitoring and logging

---

## 1. PROJECT OVERVIEW

- **Role**: Enterprise Infrastructure Engineer
- **Duration**: 2 Months
- **Environment**: Windows Server, Windows 10, Ubuntu Server, pfSense
- **Architecture**: Segmented enterprise network
- **Objective**: Build a production-style secure infrastructure

---

## 2. NETWORK ARCHITECTURE

### Network Segmentation

| Zone | Subnet          | Purpose                     |
| ---- | --------------- | --------------------------- |
| LAN  | 192.168.0.0/24  | Internal systems            |
| DMZ  | 192.168.10.0/24 | Public services             |
| MGMT | 192.168.20.0/24 | Monitoring & administration |

![pfSense Dashboard - Interfaces LAN/DMZ/MGMT](./assets/01-network-architecture.png)

---

## 3. EDGE FIREWALL SECURITY

- Firewall platform: pfSense

- **Implemented Features**:
  - Source NAT (SNAT)
  - Destination NAT (DNAT)
  - Port forwarding
  - WAN rule validation
  - Traffic filtering

![SNAT Configuration](./assets/02-nat-outbound.png)

![Port Forward Rules](./assets/03-port-forward-rules.png)

![WAN Firewall Rules](./assets/04-firewall-wan-rules.png)

---

## 4. REMOTE ACCESS VPN

- OpenVPN configured
- TLS encryption enabled
- RADIUS authentication integrated
- Secure external access validated

![Remote Access VPN](./assets/05-OpenVPN-Server-Configuration.png)

![Remote Access VPN](./assets/06-radius-authentication-test.png)

![Remote Access VPN](./assets/07-radius-authentication-successful.png)

![Remote Access VPN](./assets/08-radius-authentication-test-failed.png)

![Remote Access VPN](./assets/09-radius-authentication-failed.png)

![Remote Access VPN](./assets/10-Successful-VPN-Connection_Log.png)

---

## 5. INTRUSION DETECTION SYSTEM

- Suricata IDS deployed on WAN interface
- Enabled on WAN interface
- Real-time monitoring
- Alert logging

![Suricata Interface](./assets/11-Suricata-Interfaces.png)

![Suricata Alerts](./assets/12-Suricata-Alerts.png)

---

## 6. WEB SECURITY & PROXY FILTERING

- Transparent web proxy implemented using Squid for traffic control and logging.
- Access Control Lists (ACLs) configured
- Web traffic logging enabled
- Domain filtering with SquidGuard

![Squid ACL](./assets/13-ACLs.png)

![Access Denied](./assets/14-Access-Denied.png)

![SquidGuard Blacklist](./assets/15-SquidGuard.png)

![SquidGuard Blacklist](./assets/16-Blacklist.png)

---

## 7. ACTIVE DIRECTORY DEPLOYMENT

- Domain Controller running on Active Directory

- Installed Roles:
  - AD DS
  - DNS
  - DHCP
  - Group Policy
  - File Services
  - WSUS

![Server Roles](./assets/17-server-roles.png)

---

## 8. ACTIVE DIRECTORY STRUCTURE

### Organizational Units

![OU Structure](./assets/18-ou-structure.png)

### Security Groups

![Security Groups](./assets/19-security-groups.png)

---

## 9. GROUP POLICY HARDENING

### Password Policy

- 12+ characters
- Complexity enabled
- 90-day expiration

### Account Lockout

- 5 failed attempts
- 15-minute lockout

### Advanced Audit Policy

- Enabled for:
  - Logon events
  - Account management
  - Policy changes
  - System integrity

![Password Policy GPO](./assets/20-password-policy.png)

![Account Lockout](./assets/21-password-policy.png)

![Account Lockout](./assets/22-password-policy.png)

![Account Lockout](./assets/23-password-policy.png)

![Advanced Audit Policy](./assets/24-audit-policy.png)

---

## 10. PATCH MANAGEMENT

- Using Windows Server Update Services
  - Update synchronization configured
  - Test group created
  - Controlled deployment process

![WSUS Dashboard](./assets/25-wsus-Synchronization-Status.png)

![WSUS Dashboard](./assets/26-wsus-All-Computers.png)

---

## 11. ENDPOINT SECURITY

### Windows 10

- Domain joined
- Managed via GPO

![Domain Join](./assets/27-domain-join.png)

### BitLocker

- Enabled via Group Policy
- Recovery key stored in AD

![BitLocker Status](./assets/28-BitLocker.png)

![BitLocker Status](./assets/29-BitLocker.png)

![BitLocker Status](./assets/30-Bitlocker.png)

![BitLocker Status](./assets/31-BitLocker.png)

---

## 12. DMZ INFRASTRUCTURE

- Ubuntu Server deployed in DMZ
- NGINX web server installed
- HTTPS enabled
- Public website hosted

![Public Website](./assets/32-public-website.png)

---

## 13. MONITORING

- Monitoring tools:
  - Zabbix
  - Grafana

- Monitored:
  - CPU
  - RAM
  - Disk
  - Service availability

![Zabbix Dashboard](./assets/33-Zabbix-Dashboard.png)

![Grafana Dashboard](./assets/34-Grafana-Dashboard.png)

---

## 14. SKILLS DEMONSTRATED

- Enterprise infrastructure design
- Network segmentation
- Firewall configuration
- VPN deployment
- Identity management
- Group Policy hardening
- Patch management
- Endpoint security
- IDS implementation
- Monitoring and alerting

---

## 15. CONCLUSION

- This project demonstrates a production-style enterprise infrastructure with:
  - Centralized identity management
  - Layered security architecture
  - Segmented network design
  - Secure remote access
  - Endpoint protection
  - Patch lifecycle management
  - Continuous monitoring

- It reflects real-world enterprise security principles suitable for medium and large organizations.
