# d2allm
cd scripts/infer_pipeline/commit_msg_analyzer/
～enter msg_analyzer_llm.py
～set base_url 2 https://svip.xty.app/v1
~set api_key 2 sk...
~set authorization token with git api token (???)
python3 ./msg_analyzer_llm.py
~FFmpeg : "We run the differential analysis on thousands of selective consecutive version pairs from OpenSSL, FFmpeg, libav, httpd, NGINX and libtiff."
~fetch_commit_msg()
    ~create repo under scripts/infer_pipeline/commit_msg_analyzer/
    ~git clone FFmpeg into repo, can be reused
    ~under repo(FFmpeg git) log git commit history with pretty format (commit hash, commit date, commit content)
        git log --pretty=format:%H%s%n%b
    ~dump into variable rest
~create_chat()
    ~prompt for openai
## /Users/jingzhan/D2A-llm/scripts/infer_pipeline/commit_msg_analyzer/msg_analyzer_llm.py 运行时常
正常，我写的那个脚本调大模型的速度挺慢的，得跑一晚上才跑完，所以我一般就挂一个tmux慢慢跑。
我不太清楚调api的速度能不能更快，就在msg_analyzer_llm.py里的主函数，我是单线程按收集到的commit顺序一个个调的，所以可能比较慢？这方面不太了解
## git api token
![alt text](image.png)
这个没问题了，这边命令行输出两个dumped就说明git方面的工作结束了





