<h1 align="center"> CSE323 (OPERATING SYSTEMS DESIGN): Project </h1>
<h2 align="center"> USB Access Control
<p align="center">
 <img alt="Languages" src="https://img.shields.io/github/languages/count/haiderCho/CSE323-Project-UAC">
 <img alt="Repository size" src="https://img.shields.io/github/repo-size/haiderCho/CSE323-Project-UAC">
 <img alt="Contributors" src="https://img.shields.io/github/contributors/haiderCho/CSE323-Project-UAC">
 <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/haiderCho/CSE323-Project-UAC">
</p>
</h2>

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

---

**Project Overview: USB Device Access Control System**

This project attempts to present a comprehensive solution for managing access to USB devices through the integration of a hardware fingerprint system. This system is designed to offer enhanced security measures for organizations by regulating the utilization of USB devices, thereby mitigating risks associated with unauthorized access and potential security breaches, such as drop drive attacks.

### **Functionality:**

1. **Whitelist Management:**
   - System administrators have the authority to establish a whitelist of approved USB devices, which is stored within the control server's database.

2. **Access Control:**
   - Upon insertion of a whitelisted USB device into a machine, full access privileges are granted to the connected device.

3. **Blacklist Enforcement:**
   - In the event of a blacklisted USB device insertion:
     - Immediate unmounting of the unauthorized device.
     - Logging of the unauthorized access in the control server's database.
     - Real-time notification dispatched to the user's Android smartphone, alerting them of the unauthorized event.
     - Persistent unauthorized entries trigger a series of security measures:
       - Activation of a system-wide USB lockdown, accompanied by an audible alarm.
       - Only authorized personnel, namely the system administrator and the user, possess the capability to deactivate the alarm and lift the lockdown, facilitated through the admin panel and designated Android application, respectively.

4. **Whitelist Expansion:**
   - Addition of new USB devices to the whitelist requires authentication via the desktop application's admin panel.
   - Upon initiating the "Add to Whitelist" process, users are prompted to insert the new USB device.
   - Following successful insertion, the device's fingerprint is registered and updated within the control server's database, with a confirmation message displayed upon completion.


### **Limitations:**

Despite its robust functionality, the USB Device Access Control System has certain limitations:

- **Physical Security:** While the system effectively regulates USB device access, it does not prevent physical attacks or unauthorized data removal through means such as device tampering or theft.

- **HID Device Detection:** Detection of Human Interface Device (HID) devices is not within the scope of the system, potentially leaving certain classes of USB devices undetected.

- **Platform Compatibility:** Presently, the system is designed to operate exclusively on Windows platforms and does not support Linux, Mac, or *BSD environments.

### **Pending Enhancements:**

While the current implementation offers robust functionality, there are areas for further improvement:

- **USB Serial Number Retrieval:** Efforts are underway to enhance the system's capability to retrieve USB device serial numbers. However, challenges exist, as some methods may yield inconsistent results, particularly after device reformatting.

- **Email Configuration:** Future iterations of the system will aim to support a broader range of email configuration use cases, including compatibility with open authentication mail servers, thereby enhancing flexibility and usability.

These ongoing efforts underscore our commitment to continually enhancing the USB Device Access Control System to meet evolving security needs and user requirements.

### Security Concern 
- **Keystroke Capture:** The system does not include features to capture keystrokes upon USB device insertion or removal, limiting its ability to monitor user interactions.

### **Conclusion:**

The USB Device Access Control System demonstrates a proactive approach towards bolstering organizational security measures by efficiently managing USB device access. By combining hardware fingerprint technology with robust access control protocols and real-time monitoring capabilities, the system offers a robust defense against potential security threats, ensuring the integrity and confidentiality of sensitive data within enterprise environments.