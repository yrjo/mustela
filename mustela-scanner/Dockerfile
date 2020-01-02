FROM centos:7

RUN yum update --assumeyes --skip-broken && \
      yum -y install epel-release nmap git gcc make libpcap-dev libxslt libpcap libpcap-devel \
      python3 pip3 python-argparse python-dnspython python-requests python-dns\
      yum clean all


RUN cd /opt && git clone https://github.com/robertdavidgraham/masscan
RUN cd /opt && git clone https://github.com/aboul3la/Sublist3r
RUN cd /opt && git clone https://github.com/nabla-c0d3/sslyze
RUN cd /opt && git clone https://github.com/ernw/nmap-parse-output


#RUN pip3 install --upgrade setuptool
RUN pip3 install --upgrade sslyze

RUN cd /opt/masscan && make -j
