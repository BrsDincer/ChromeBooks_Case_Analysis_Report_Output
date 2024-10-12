
# Cross-Border Data Transfers in Education: Investigating Google Chromebooks in Danish Schools

## Overview

This repository provides a detailed analysis of **cross-border data transfers** occurring through **Google Chromebooks** distributed in Danish schools. The focus is on determining whether student data, including **internet usage patterns**, is being transferred from **Europe to U.S.-based servers**. The investigation leverages network traffic analysis using tools like **Wireshark** and **Tshark** to assess the data flow to Google and other CDN services.

## Objectives

- **Analyze Network Traffic**: Identify if children’s personal data is transferred from Chromebooks to servers located in the United States.
- **Evaluate GDPR Compliance**: Assess whether such transfers adhere to **General Data Protection Regulation (GDPR)** requirements.
- **Provide Legal Evidence**: Present findings that can be used in legal or regulatory contexts regarding privacy violations.

## Key Findings

1. **Substantial QUIC Traffic**: A significant portion of the traffic uses the **QUIC protocol**, particularly associated with **Google services** such as **Google Classroom**, **Google Drive**, and **YouTube**. This raises concerns about **cross-border data transfers** and privacy risks.
   
2. **U.S.-Based Servers**: Traffic was found to be directed toward **U.S.-based data centers**, including those in **Kansas City** and **Los Angeles**. This suggests the transmission of **student data** to servers outside the EU, potentially violating GDPR’s cross-border data transfer regulations.

3. **Involvement of Other CDN Providers**: Services like **Akamai** and **Cloudflare** were identified as intermediaries in data transfer, further complicating **data sovereignty** issues.

4. **Advertising and Tracking**: Interaction with **Google Ads** and **Google Analytics** raises concerns about the **tracking of students’ activities**, potentially violating GDPR and other privacy protections related to minors.

5. **Encryption and Privacy**: While traffic is often encrypted (e.g., **TLS**, **QUIC**), this raises issues about the **lack of transparency** in what data is being transferred and how it is being handled.

[View Endpoint Map IPv4 Raw](endpoint_map_ipv4.html)

[View Endpoint Map UDP Raw](endpoint_map_udp.html)

## Tools Used

- **Wireshark / Tshark**: For packet capture and analysis.
- **Geolocation Services**: To track the locations of the servers interacting with the Chromebooks.
- **Cryptographic Hashes**: Used to verify data integrity and ensure no tampering with the packet capture files.

## Legal Considerations

- **GDPR Non-Compliance**: Data transfers to non-EU servers without adequate protection measures (like **Standard Contractual Clauses (SCCs)**) could be in violation of GDPR.
- **Student Privacy**: The use of student data in advertising or tracking services, especially without proper consent, raises significant privacy concerns under GDPR’s special provisions for minors.
- **Cross-border Surveillance**: Data transferred to U.S.-based servers may be subject to **U.S. surveillance laws** like **FISA** and **Executive Order 12333**, conflicting with GDPR protections.

## Recommendations

1. **Conduct Data Protection Impact Assessments (DPIAs)**: Educational institutions should assess the risks associated with the use of **Google services** and **CDN providers**.
2. **Verify GDPR Compliance**: Ensure that proper **legal mechanisms** (e.g., SCCs) are in place for any data transfers outside the EU.
3. **Data Minimization and Encryption**: Minimize the amount of personal data transferred and apply **strong encryption** and **anonymization** techniques.
4. **Transparency and Consent**: Obtain clear, informed consent from students or their guardians for data processing activities involving non-EU data transfers.

## Repository Structure

- **Packet Captures**: Sample `.pcapng` files used in the analysis.
- **Scripts**: Example scripts used for traffic analysis with **Tshark** and **Wireshark**.
- **Report**: The full report documenting the findings and legal implications.

