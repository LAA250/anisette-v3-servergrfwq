# anisette-v3-server

A supposedly lighter alternative to [omnisette-server](https://github.com/SideStore/omnisette-server)

Like `omnisette-server`, it supports both currently supported SideStore's protocols (anisette-v1 and 
anisette-v3) but it can also be used with AltServer-Linux.

## Run using Docker

```bash
docker run -d --restart always --name anisette-v3 -p 6969:6969 --volume anisette-v3_data:/home/Alcoholic/.config/anisette-v3/lib/ dadoum/anisette-v3-server
```

## Compile using dub

```bash
apt update && apt install --no-install-recommends -y ca-certificates ldc git clang dub libz-dev libssl-dev
git clone https://github.com/Dadoum/anisette-v3-server.git; cd anisette-v3-server
DC=ldc2 dub build -c "static" --build-mode allAtOnce -b release --compiler=ldc2
stat anisette-v3-server
```

## Ansible

If you want to quickly setup anisette-v3 with ansible, just use the setup-anisette-v3-ansible.yaml playbook.
Setup your inventory and choose your desired host in the playbook. Tweak your parameters/ansible.cfg for the remote_user you use. Requires root.
```bash
ansible-playbook -i inventory setup-anisette-v3-ansible.yaml -k
```


以下是中文机翻

Anisette-v3-服务器

所谓的omnisette-server的更轻的替代品

与omnisette-server一样，它支持目前支持的SideStore协议（anisette-v1和anisette-v3），但它也可以与AltServer-Linux一起使用。

使用Docker运行

Docker run -d --restart always --name anisette-v3 -p 6969:6969 --volume anisette-v3_data:/home/Alcoholic/.config/anisette-v3/lib/ dadoum/anisette-v3-server

使用配音编译

Apt update && apt install --no-install-recommends -y ca-certificates ldc git clang dub libz-dev libssl-dev

git克隆https://github.com/Dadoum/anisette-v3-server.git；cd anisette-v3-server

DC=ldc2配音构建-c“静态”--构建模式allAtOnce-b发布--编译器=ldc2

统计anisette-v3-服务器

安西

如果您想使用ansible快速设置anisette-v3，只需使用setup-anisette-v3-ansible.yaml游戏手册。 设置您的库存，并在游戏手册中选择您想要的主机。 为您使用的远程用户调整参数/ansible.cfg。 需要根。

Ansible-playbook -i 库存设置-anisette-v3-ansible.yaml -k