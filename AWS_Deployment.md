 Log in to your AWS console and search for EC2
 - In the EC2 create a instance t2.tiny configuration ubuntu x86 image and launch the instance.
 - Clone the repo : git clone < git-repo-url >.
 - Change directory to the project's root folder.
 - Install docker and node.js via NVM on the instance.
 - Install dependencies : npm install.
 - Run the docker container with the built image : ```docker run -p 3000:3000 -e OPENAI_API_KEY=<your-api-key> -e ALLOWED_RAM=<allowed-ram-value> <image-name>``` , generate open-API key and replace the constant for RAM.
 - Add Custom TCP configuration with port 3000 and inbount 0.0.0.0/0.
 - Open postman and try to make a POST request on with given payload ```http://<instance-ipv4>:3000/api/execute/``` using the payload provided in ```README.md```

 ### Example

 <img width="756" alt="Post-man" src="https://github.com/aryanraj2713/compilerd/assets/75358720/a556942e-b142-48c5-af91-49bdc17ebe77">