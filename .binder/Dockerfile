FROM jupyter/scipy-notebook:latest

# 安装 RDKit
RUN conda install -c conda-forge rdkit
RUN pip install --pre deepchem
    
# 复制所有文件到 /home/jovyan/work
COPY ./data /home/jovyan/work

# 设置工作目录，使 Jupyter 直接打开 /home/jovyan/work
WORKDIR /home/jovyan/work

# 确保 Notebook 启动目录正确
CMD ["start-notebook.sh", "--NotebookApp.token=''"]
