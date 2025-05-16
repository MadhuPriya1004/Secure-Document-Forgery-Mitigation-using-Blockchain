# Secure-Document-Forgery-Mitigation-using-Blockchain
This project aims to mitigate the risks of document forgery by leveraging the immutability of blockchain technology combined with secure storage on IPFS and robust Google-based authentication using Firebase. It ensures document integrity, prevents duplicates, and enables secure issuing and verification, along with email-based notifications for previous contributors.

# Features

**Decentralized Storage:** Stores document metadata and hash on Ethereum blockchain using a custom smart contract.

**IPFS Integration**: Actual documents are uploaded to InterPlanetary File System (IPFS) to ensure decentralized file hosting.

**Forgery Detection:** Prevents re-upload of previously submitted documents by checking file hashes.

**Role-Based Access:** Controlled issuing of documents using Firebase-authenticated user roles.

**Masked Email Notifications:** Uses EmailJS and AbstractAPI to notify all previous uploaders/issuers with masked metadata.

**QR Code Generation:** Issues documents with scannable QR codes pointing to IPFS download links.

**User Authentication:** Secured login via Firebase Google OTP Authentication (no email input required).

**Blockchain Event Handling:** Listens to contract events in real-time and reacts on the frontend using Web3.js

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

# Folder Structure

secure-doc-project/
├── contracts/
│   └── DocumentStorage.sol          # Smart contract logic
├── public/
├── src/
│   ├── components/
│   │   ├── UploadDocument.js        # Uploads document, triggers notifications
│   │   ├── IssueDocument.js         # Issues documents and notifies prior users
│   │   ├── VerifyDocument.js        # Verifies documents using hash & QR
│   │   ├── Dashboard.js             # User dashboard
│   │   ├── AboutUs.js               # Project & team information
│   │   ├── ContactUs.js             # Team contact cards with hover effects
│   └── App.js                       # Main app routing
├── package.json
├── truffle-config.js
└── README.md

# Installation & Setup Instructions

**1. Clone the Repository**
   git clone https://github.com/your-username/secure-doc-blockchain.git
   cd secure-doc-blockchain
**2. Install Dependencies**
   npm install
**3. Start Ganache GUI**
   Open Ganache GUI and create a new workspace.
   Use the RPC port in your truffle-config.js file.
**4. Compile and Deploy Smart Contract**
   truffle compile
   truffle migrate
**5. Start the React App**
   npm start

**EmailJS Configuration**
   You need to set up EmailJS templates as follows:

# Templates Used:
template_5zkkkh — For previous uploader notifications
template_567ghy — For confirmation email to the uploader
Service ID: service_mpyyy1b
Public Key: jmai8_hA9LSllllj

# Variables used in the templates:
document_name
uploader_email
upload_time
to_email
name
email

# WorkFlow:
**Upload Flow:**

User uploads a document → Hash generated.

Hash is checked on-chain to prevent duplicates.

If new, it's uploaded to IPFS, hash + metadata saved on-chain.

Previous uploaders notified with masked details.

**Issue Flow:**

Document is sent to a receiver via email with IPFS link.

Previous uploaders are notified.

Access is validated using Firebase authentication.

**Verify Flow:**

Document hash or QR scanned and checked against blockchain records

# UI Features
Modern, clean React interface

Role-based navigation (Upload/Issue/Verify)

Real-time event listening from blockchain

Contact Cards with hover effects

QR code preview before issuing

Smooth navigation between all modules

# Contributors
Madhu Priya – GCET, Roll No: 22R15A0505 – 22R15A0505@gcet.edu.in

Sania – GCET, Roll No: 21R11A0548 – 21R11A0548@gcet.edu.in

Swapnil – GCET, Roll No: 22R15A0502 – 22R15A0502@gcet.edu.in

 # License
This project is for educational and academic purposes only.

