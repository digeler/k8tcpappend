# k8tcpappend -multiple append files k8s tcpdumper
Create a storage accoutn in you MC_ rg
Clone the the repo with git clone https://github.com/digeler/k8tcpappend.git
extract the file tar -xvf kubecaptureappend-0.1.0.tgz
install the chart by : helm install kubecaptureappend --set sa=[yourstorageaccount]
edit the the reclaim policy of the pv by kubeclt edit pv change delete to retain ,this will prevent deletion of the traces , when you stop the trace.
this will create 40 files of 500m for each node ,rotating when the first one is full.
when you want to stop the trace just remove the deployment files will still be there -by helm delete deployment

