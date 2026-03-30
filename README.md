# bashrc
~/.bashrc

# 激活 PolarFire RISC-V 交叉编译环境
```bash
env_riscv() {
    source /opt/riscv/environment-setup-riscv64-mchp-linux
    export CC="riscv64-mchp-linux-gcc --sysroot=/opt/riscv/sysroots/riscv64-mchp-linux"
    echo "✅ PolarFire RISC-V 环境已完全就绪。"
}
```

# 开启终端代理
```bash
proxy_on() {
    export http_proxy=http://127.0.0.1:1080
    export https_proxy=http://127.0.0.1:1080
    # 增量细节：很多底层 C/C++ 工具和 Git 实际上认的是 all_proxy
    export all_proxy=socks5://127.0.0.1:1080 
    echo "🟢 终端代理已开启"
}
```

# 彻底清除终端代理
```bash
proxy_off() {
    unset http_proxy
    unset https_proxy
    unset all_proxy
    echo "🔴 终端代理已关闭"
}
```
