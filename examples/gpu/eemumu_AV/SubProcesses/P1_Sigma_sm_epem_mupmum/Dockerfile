FROM nvidia/cuda:10.2-devel-ubuntu18.04

RUN apt-get update && apt-get install -y gcc-8 git

RUN git clone https://github.com/madgraph5/madgraph4gpu.git

WORKDIR madgraph4gpu/examples/gpu/eemumu_AV/SubProcesses/P1_Sigma_sm_epem_mupmum

RUN make

CMD ["-p", "4096", "32", "64"]

ENTRYPOINT ["/madgraph4gpu/examples/gpu/eemumu_AV/SubProcesses/P1_Sigma_sm_epem_mupmum/gcheck.exe"]
