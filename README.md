# logstash-wireshark-tlsnames
Get wireshark/tshark tls logs in JSON format to elasticsearch with logstash

Create Logstash Output with tshark from command line:

sudo tshark -Y ssl.handshake.extensions_server_name -T ek -e ssl.handshake.extensions_server_name -e ip.src -e ip.dst -e frame.time >/tmp/tlsnames
