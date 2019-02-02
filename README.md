# k8tcpappend -multiple append files k8s tcpdumper
Create a storage accoutn in you MC_ rg
Clone the the repo with git clone https://github.com/digeler/k8tcpappend.git
extract the file tar -xvf kubecaptureappend-0.1.0.tgz
install the chart by : helm install kubecaptureappend --set sa=[yourstorageaccount]
this will create 40 files of 500m for each node ,rotating when the first one is full.
