
# SSH Brutefrocer Toolkit

A Python-based toolkit for performing SSH authentication testing using brute-force techniques. This project includes two scripts:
- `ssh_brute.py` → Basic single-threaded password brute-forcing.
- `advanced_ssh_brute.py` → Multi-threaded and flexible brute-force tool with password generation support.



## Features

**Basic Script** `ssh_bruteforcer.py`
- Simple password brute-force using a wordlist
- SSH connection handling with retries
- Stops on first successful login

**Advanced Script** `advanced_ssh_bruteforcer.py`
- Multi-threaded brute forcing
- Username and password list support
- On-the-fly password generation
- Queue-based worker system
- Configurable thread count
- Faster and more flexible


## Requirements

- Python 3.x
- Required libraries:
```bash 
pip install -r requirements.txt
```
## Usage

1. **Basic Bruteforce** 

```bash 
python ssh_bruteforcer.py <host> -u <username> -P <password_list>
```

- **Example:**
```bash 
python ssh_bruteforcer.py 192.168.1.10 -u root -P passwords.txt 
```

2. **Advanced Bruteforce**
- Using password list
```bash 
python advanced_ssh_bruteforcer.py <host> -u <username> -P <password_list> -t <threads> 
```
- Using username list
```bash 
python advanced_ssh_bruteforcer.py <host> -U users.txt -P passwords.txt -t 10 
```
- Generating passwords
```bash 
python advanced_ssh_bruteforcer.py <host> -u root -g --min_length 4 --max_length 6 -c abc123
```
### Arguments


### Output

- Successful credentials are saved in: credentials.txt