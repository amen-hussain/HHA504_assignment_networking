# HHA504_assignment_networking
Assignment: Networking in Azure and GCP - IPs and Domain Management

#### 1. Create a Virtual Private Cloud (VPC)
- **Azure:**
  - Navigate to the Azure portal and create a new Virtual Network (VNet).
  - Choose a simple IP address range and subnet configuration.
 <img width="695" alt="image" src="https://github.com/user-attachments/assets/6d025ba2-2d61-484f-b6d3-c6223c371753">
<img width="816" alt="image" src="https://github.com/user-attachments/assets/9d378573-1dc5-43f7-982b-73adc0476d56">
<img width="789" alt="image" src="https://github.com/user-attachments/assets/049e0a7a-aa4f-466d-a0fb-783f1c401459">
<img width="518" alt="image" src="https://github.com/user-attachments/assets/881fe0b2-7507-4100-b7c4-a2e22100ae86">



  
- **GCP:**
  - Access the Google Cloud Console and create a new VPC network.
  - Configure the IP address range and subnets similarly to your Azure setup.


#### 2. Assign a Dedicated or Dynamic IP
- **Azure:**
  - You may either reserve a static public IP address for a resource (e.g., a virtual machine) within your VNet or use the dynamic public IP assigned by Azure.
 <img width="780" alt="image" src="https://github.com/user-attachments/assets/ec63326f-b671-4725-b372-ba7b470fc4b5">
  
- **GCP:**
  - Reserve a static external IP address for a Compute Engine instance within your VPC or use the dynamically assigned public IP.

#### 3. Map IP to a Domain Acquired via GitHub Student Pack
- Use your GitHub Student Developer Pack to acquire a domain through Namecheap (or another supported registrar).
<img width="631" alt="image" src="https://github.com/user-attachments/assets/9a01a76d-06ae-49f1-93b6-cd5735bb50f3">
<img width="636" alt="image" src="https://github.com/user-attachments/assets/ff69bc92-205a-479b-b457-ce70c3f549f1">
<img width="512" alt="image" src="https://github.com/user-attachments/assets/51b1df3a-9b21-41b3-b280-e1c8a986d94a">
<img width="470" alt="image" src="https://github.com/user-attachments/assets/707912f1-e51b-49ce-9128-cd308b80f72c">
<img width="600" alt="image" src="https://github.com/user-attachments/assets/cc010363-018f-4cca-9e84-027643f65a52">
<img width="430" alt="image" src="https://github.com/user-attachments/assets/9190f094-35e0-40bc-9f4f-af79e906c6c7">
<img width="709" alt="image" src="https://github.com/user-attachments/assets/f48fac3b-2acc-4e6b-aed6-4a6549e56965">

  
- Set up an **A record** for your main domain (e.g., `yourdomain.com`) and a **subdomain** (e.g., `app.yourdomain.com`).

#### 4. Deploy Flask Application
- Deploy the provided Flask application located at [HHA 504 Flask Networking](https://github.com/hantswilliams/hha-504-flask-networking) to your virtual machine on Azure or GCP.
- Ensure that the Flask application is running on a specific port (e.g., port 5007).

#### 5. Configure Firewall Settings
- Make sure that the port on which your Flask application is running is accessible to the general public.
  - **Azure:** Configure Network Security Group (NSG) rules to allow inbound traffic on the specified port.
  - **GCP:** Configure Firewall rules to allow traffic on the specified port.

#### 6. Access Your Application via Domain
- Visit your deployed Flask application using the custom domain or subdomain you mapped, including the port number in the URL (e.g., `http://app.yourdomain.com:5000`).
  
#### 7. Submit Your Work
- Create a Markdown document that includes:
  - Screenshots of the VPC/VNet creation and IP reservation process in both Azure and GCP.
  - Screenshots and documentation of the steps taken to map the IP address to the domain (including the creation of A records and subdomains).
  - Screenshots of the running Flask application accessible via your domain or subdomain.
  - Documentation on how you configured the firewall rules to allow access to the Flask app.
- Errors 
  - As usual, if you run into errors, document them and how you attempted to resolve them.
  - It is ok if you are unable to resolve the errors, document what you tried and what you think the error might be.

- Commit and push this Markdown document, along with the screenshots, to your GitHub repository.

### Deliverables
- A Markdown document in a GitHub repository called `HHA504_assignment_networking` that includes:
  - Screenshots of VPC/VNet creation and IP reservation.
  - Steps and screenshots for mapping IPs to domains and configuring subdomains.
  - Screenshots of the Flask app running and accessible via the mapped domain or subdomain.
  - Firewall rule configurations that allow public access to the Flask application.
