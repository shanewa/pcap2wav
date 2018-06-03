# pcap2wav
A simple utility to make it easier to extract the audio from a pcap.
The outputs are named by the SSRC.
  
USAGE:
    pcap2wav [ -h|--help ]
    pcap2wav -r|--read <pcap file> [-m|--mix] [-p|--path]

extended_usage=
    --help, -h              : Displays command usage.
    

    --read, -r <pcap file>  :  Load a pcap file
    
    
    --mix, -m               : Combine/mix the two-way voice into one wav file
    
    
    --path, -p              : Move the generated wav files to this path
    

EXAMPLES:
    pcap2wav --help
    
    pcap2wav -r SIP_call_with_RTP_in_G711.pcap
    
    pcap2wav -r SIP_call_with_RTP_in_G711.pcap -p /root/wav
    
    pcap2wav -r SIP_call_with_RTP_in_G711.pcap -p /root/wav --mix
    
        
Dependencies:

   apt-get install -y tshark sox
   
   yum install wireshark sox
