#Note
This repository is no longer maintained, a alternative tool similar to this can be found here: [`https://github.com/AvinashSingh786/SecureRS`](SecureRS).

<img src="https://github.com/AvinashSingh786/W3RS/raw/master/static/assets/img/w3rs.png" height="150" width="350"/>
  
 
## Windows Registry and RAM  Readiness Storage (W3RS)
This tool was designed for research in the field of Digital Forensics.

This prototype solution was created with Digital Forensic Readiness processes for secure storage and retrieval or potential digital evidence. This solution is generic and can be used for any application  that requires secure storage. There is also an API built in that allows integration with any system or tool. From the admin panel you can create and manage API keys and routes.
  
This prototype tool is the secure storage engine for the overall framework Ransomware Readiness Framework (2RF) (publications below). There is some significant setup that needs to be done in order to get the analysis engine up and running. The [`installation guide`](https://github.com/AvinashSingh786/W3RS/raw/master/Installation_Guide.pdf).  

## Installation
This tool can be run from a docker container that can be built using the dockerfile. Alternatively, you can clone this repository and install the python requirements. It is recommended you run this in a virtual environment to further ensure compatibility and added security. More details on this can be found in the [`installation guide`](https://github.com/AvinashSingh786/W3RS/raw/master/Installation_Guide.pdf).  
```bash
git clone git@github.com:AvinashSingh786/W3RS.git
cd W3RS
pip install -r requirements.txt
```


## Usage
Run the following commands to configure and run the engine.

```bash
(venv)$ python manage.py createsuperuser  # Create a super user that you will use as the admin
(venv)$ python manage.py makemigrations   # This sets up the storage engine and databases
(venv)$ python manage.py migrate          # This creates the databases and interfaces
(venv)$ python manage.py runsslserver 0.0.0.0:8000  
``` 

## IMPORTANT
If you plan on using this tool in production please change the following in the settings.py file:
- SECRET_KEY
- DEBUG
- EMAIL_USE_TLS 
- EMAIL_HOST 
- EMAIL_PORT
- EMAIL_HOST_USER
- EMAIL_HOST_PASSWORD
 
Below are screenshots of the tool.
<img src="https://github.com/AvinashSingh786/W3RS/raw/master/static/assets/img/home.png" />
<img src="https://github.com/AvinashSingh786/W3RS/raw/master/static/assets/img/details.png" />
 
## Testing environments
  - Windows 10
  - Windows 8.1
  - Windows 7
  - Windows XP

## Contributing
 
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Wanted
 
  - Bug reports.
  - Feedback.


## License
 
MIT License

## Publications
*	Singh, A. R. Ikuesan, and H. S. Venter, “Digital Forensic Readiness Framework for Ransomware Investigation,” in Digital Forensics and Cyber Crime, 2019, pp. 91–105.

*	A. Singh, A. Ikuesan, and H. Venter, “A context-aware trigger mechanism for ransomware forensics,” 14th Int. Conf. Cyber Warf. Secur. ICCWS 2019, pp. 629–638, 2019.
