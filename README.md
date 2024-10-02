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
<img width="701" alt="image" src="https://github.com/user-attachments/assets/71fd0c34-6219-4264-b897-8e34b90f6d11">
<img width="631" alt="image" src="https://github.com/user-attachments/assets/092bf7fe-d99c-4b87-9bf6-d6b02aee305b">
<img width="637" alt="image" src="https://github.com/user-attachments/assets/09090a8d-28a3-48c9-8241-6666c75980e2">
<img width="1246" alt="image" src="https://github.com/user-attachments/assets/03765287-1f40-4458-9a69-82b0a626ddde">
<img width="1261" alt="image" src="https://github.com/user-attachments/assets/0701ad73-9835-4ee4-b825-9d5698a8a0ef">




#### 2. Assign a Dedicated or Dynamic IP
- **Azure:**
  - You may either reserve a static public IP address for a resource (e.g., a virtual machine) within your VNet or use the dynamic public IP assigned by Azure.
 <img width="780" alt="image" src="https://github.com/user-attachments/assets/ec63326f-b671-4725-b372-ba7b470fc4b5">
  <img width="1337" alt="image" src="https://github.com/user-attachments/assets/98fcfa38-6540-4fa3-a671-911306b234f6">

- **GCP:**
  - Reserve a static external IP address for a Compute Engine instance within your VPC or use the dynamically assigned public IP.
<img width="1330" alt="image" src="https://github.com/user-attachments/assets/32621ea0-6473-44c5-9239-10ad5afe6020">



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
<img width="1037" alt="image" src="https://github.com/user-attachments/assets/1cec982b-d9e4-408a-a42c-be12b0336fd9">



#### 4. Deploy Flask Application
- Deploy the provided Flask application located at [HHA 504 Flask Networking](https://github.com/hantswilliams/hha-504-flask-networking) to your virtual machine on Azure or GCP.
- Ensure that the Flask application is running on a specific port (e.g., port 5007).
<img width="1181" alt="image" src="https://github.com/user-attachments/assets/942818b8-af9c-4b49-83ec-302337225c6a">
<img width="944" alt="image" src="https://github.com/user-attachments/assets/15941057-cd47-46fc-a6d1-8a67441f0e1b">



#### 5. Configure Firewall Settings
- Make sure that the port on which your Flask application is running is accessible to the general public.
  
  - **Azure:** Configure Network Security Group (NSG) rules to allow inbound traffic on the specified port.
 <img width="776" alt="image" src="https://github.com/user-attachments/assets/74d107e1-c27d-4436-a2d0-b5a869d2519e">

  
  - **GCP:** Configure Firewall rules to allow traffic on the specified port.
<img width="905" alt="image" src="https://github.com/user-attachments/assets/4c35c8b0-dfcb-4675-be4f-a86403789ab4">

<img width="775" alt="image" src="https://github.com/user-attachments/assets/549e41af-28ec-4465-be0f-b85f42d4cb1c">
<img width="528" alt="image" src="https://github.com/user-attachments/assets/e550fd45-0420-453d-842e-91cf27f7af9e">


#### 6. Access Your Application via Domain

  
### Errors 
On Azure I was unable to "Configure Network Security Group (NSG) rules to allow inbound traffic on the specified port" for my virtual network. The photo I attached shows how I would be able to adjust those settings when creating a virtual machine on azure instead. In the virtual network, I was able to navigate to a firewall tab that allowed me create a new one, however I had trouble doing so. 
<img width="725" alt="image" src="https://github.com/user-attachments/assets/e2de5063-5c2a-4628-9902-7cc28eff5c0e">
<img width="754" alt="image" src="https://github.com/user-attachments/assets/3b90c372-9b0f-45e3-ab73-23275a6ab534">

Additionally, when creating a VM instance on GCP, the option to change the Boot disk is not shown on my end. Therefore I was unable to alter the operating system to ubuntu which was needed to open the SSH server. 

Due to these obstacles, I was unable to move forward and complete steps 4-6. 
