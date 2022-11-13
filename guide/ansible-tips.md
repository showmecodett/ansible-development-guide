# Ansible小技巧

## Playbook添加默认值
playbook的默认值，类似于shell中的默认值，如：
```bash
hosts=${host:-all}
```

示例代码：[Playbook with default value](/project/playbook_with_default.yml)

* 执行全部主机：`ansible-playbook -i project/inventory/hosts project/playbook_with_default.yml`
* 执行部分主机：`ansible-playbook -i project/inventory/hosts project/playbook_with_default.yml --extra-vars='host=192.168.33.10'`

# 参考
* [幾個小建議改善你的 Ansible 技能](https://blog.pichuang.com.tw/20180622-suggestions_to_improve_your_ansible_playbook/)
