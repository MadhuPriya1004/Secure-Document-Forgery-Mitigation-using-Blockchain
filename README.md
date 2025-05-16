# Secure-Document-Forgery-Mitigation-using-Blockchain
This is a full-stack web application that ensures the authenticity of uploaded documents using Blockchain, IPFS, and Firebase. It prevents forgery attempts by validating document hashes and alerts prior uploaders about re-uploads or issuance via email. 

# Features

Upload documents and store their hashes on the blockchain

Validate document uniqueness via SHA-256

Upload documents to IPFS (via Pinata)

Google-based Firebase OTP authentication

Notify previous uploaders on re-upload or issuance using EmailJS

QR code generation for IPFS access

Role-based access control (Issue, Upload, Verify)

Masked data (filename and email) for privacy

UI includes About & Contact sections

# Technologies Used

| Layer             | Tools & Technologies                             |
| ----------------- | ------------------------------------------------ |
| Frontend          | React.js, HTML5, CSS3, JavaScript (No Tailwind)  |
| Backend           | Ethereum Smart Contracts (Solidity), Ganache GUI |
| Blockchain Access | Web3.js                                          |
| File Storage      | IPFS                                             |
| Authentication    | Firebase (Google OTP Auth)                       |
| Notifications     | EmailJS                                          |
| IDE               | Visual Studio Code (Windows)                     |
| Backend DB        | Firestore (to log previous uploaders)            |


