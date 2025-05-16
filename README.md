# Secure-Document-Forgery-Mitigation-using-Blockchain
This is a full-stack web application that ensures the authenticity of uploaded documents using Blockchain, IPFS, and Firebase. It prevents forgery attempts by validating document hashes and alerts prior uploaders about re-uploads or issuance via email. 

# Features

#Decentralized Storage:# Stores document metadata and hash on Ethereum blockchain using a custom smart contract.

IPFS Integration: Actual documents are uploaded to InterPlanetary File System (IPFS) to ensure decentralized file hosting.

Forgery Detection: Prevents re-upload of previously submitted documents by checking file hashes.

Role-Based Access: Controlled issuing of documents using Firebase-authenticated user roles.

Masked Email Notifications: Uses EmailJS and AbstractAPI to notify all previous uploaders/issuers with masked metadata.

QR Code Generation: Issues documents with scannable QR codes pointing to IPFS download links.

User Authentication: Secured login via Firebase Google OTP Authentication (no email input required).

Blockchain Event Handling: Listens to contract events in real-time and reacts on the frontend using Web3.js

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


