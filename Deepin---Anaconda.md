1. 使用清华镜像

    ```scss
    " 使用清华镜像源
    pip install -i https://pypi.tuna.tsinghua.edu.cn/simple
    
    " conda 使用清华镜像源
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
    conda config --set show_channel_urls yes
    ```

2. conda环境

    ```scss
    " 导出环境
    pip freeze > ~/Desktop/1.txt
    conda list -e > requirements.txt
    
    " 安装环境
    pip install -r ~/Desktop/1.txt
    conda install --yes --file requirements.txt
    
    " 加入环境变量
    
    # >>> conda initialize >>>
    # 路径会有所不同
    # !! Contents within this block are managed by 'conda init' !!
    __conda_setup="$('/home/xyy/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
    if [ $? -eq 0 ]; then
        eval "$__conda_setup"
    else
        if [ -f "/home/xyy/anaconda3/etc/profile.d/conda.sh" ]; then
            . "/home/xyy/anaconda3/etc/profile.d/conda.sh"
        else
            export PATH="/home/xyy/anaconda3/bin:$PATH"
        fi
    fi
    unset __conda_setup
    # <<< conda initialize <<<
    ```

    
