# bashrc
~/.bashrc

# 激活 PolarFire RISC-V 交叉编译环境
env_riscv() {
    source /opt/riscv/environment-setup-riscv64-mchp-linux
    export CC="riscv64-mchp-linux-gcc --sysroot=/opt/riscv/sysroots/riscv64-mchp-linux"
    echo "✅ PolarFire RISC-V 环境已完全就绪。"
}
