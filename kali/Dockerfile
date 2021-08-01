# From the Kali linux base image
FROM kalilinux/kali-rolling

# Update and apt install programs
RUN apt-get update && apt-get upgrade -y && apt-get dist-upgrade -y && apt-get install -y \
 exploitdb \
 exploitdb-bin-sploits \
 git \
 gdb \
 gobuster \
 hashcat \
 hydra \
 man-db \
 minicom \
 nasm \
 nmap \
 sqlmap \
 sslscan \
 wordlists \
 pip


# Clone git repos
RUN git clone https://github.com/danielmiessler/SecLists.git /opt/seclists
RUN git clone https://github.com/PowerShellMafia/PowerSploit.git /opt/powersploit


# Other installs
RUN pip install pwntools

# Update ENV
ENV PATH=$PATH:/opt/powersploit

