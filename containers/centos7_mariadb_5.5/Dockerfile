From centos:7

RUN yum install -y mariadb-server mariadb-devel git python-setuptools gcc python-devel
RUN yum install -y http://www.percona.com/downloads/percona-release/redhat/0.1-4/percona-release-0.1-4.noarch.rpm
RUN yum install -y percona-xtrabackup-24
RUN yum install -y https://centos7.iuscommunity.org/ius-release.rpm
RUN easy_install six
RUN easy_install future
RUN easy_install ConfigParser
RUN easy_install mysql-python
RUN git clone https://github.com/datacharmer/test_db.git
ADD ./entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
CMD /entrypoint.sh
