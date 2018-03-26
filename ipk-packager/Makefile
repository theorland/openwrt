ipk_name=dnscrypt-proxy-resolvers_1.9.5+git-20170530-60baef4-7_ramips.ipk

extract:
	tar zxpvf $(ipk_name) 
	if [ ! -d data ]; then  mkdir data; fi
	tar zxpvf data.tar.gz -C data
	if [ ! -d control ]; then mkdir control; fi
	tar zxpvf control.tar.gz -C control

pack:
	if [ -f $(ipk_name) ] ; then mv $(ipk_name) $(ipk_name).0; fi
	tar zcvf data.tar.gz  -C data .
	tar zcvf control.tar.gz -C control .
	ar r $(ipk_name)  control.tar.gz data.tar.gz  debian-binary
clean:
	rm -r control data
	rm control.tar.gz data.tar.gz  debian-binary



