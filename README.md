q# springboot-conf-gateway-api
-----------------------------------------------------

curl -X 'GET' 'http://10.0.0.137:8766/foo/' -H 'accept: */*'
curl -X 'GET' 'http://10.0.0.137:7776/foo/bar' -H 'accept: */*'
curl -X 'GET' 'http://10.0.0.137:7776/foo/foo-properties' -H 'accept: */*'
curl -X 'GET' 'http://10.0.0.137:7776/foo/bar-properties' -H 'accept: */*'
...

-----------------------------------------------------
IN "10.0.0.137" do:
-----------------------------------------------------
sudo firewall-cmd --add-port=8766/tcp --permanent
sudo firewall-cmd --reload

sudo firewall-cmd --list-ports
sudo firewall-cmd --list-all

---Fermer le port 8766 -------------------------------
sudo firewall-cmd --permanent --remove-port=7776/tcp
sudo firewall-cmd --reload

sudo firewall-cmd --list-ports
sudo firewall-cmd --list-all
-----------------------------------------------------
