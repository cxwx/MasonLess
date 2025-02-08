<!-- *********************************************************************** -->
<!--                                                                         -->
<!--                                                      :::      ::::::::  -->
<!-- README.md                                          :+:      :+:    :+:  -->
<!--                                                  +:+ +:+         +:+    -->
<!-- By: chenxu <chenxu@mail.ustc.edu.cn>           +#+  +:+       +#+       -->
<!--                                              +#+#+#+#+#+   +#+          -->
<!-- Created: 2024/11/29 16:00:26 by chenxu            #+#    #+#            -->
<!-- Updated: 2024/11/30 21:02:04 by chenxu           ###   ########.fr      -->
<!--                                                                         -->
<!-- *********************************************************************** -->
<!-- cspell:disable -->

# 删除 Mason 与 Homebrew 重叠的部分

## 查看

```zsh
gls -l /opt/homebrew/bin ~/software/gopath/bin ~/software/npm/install/bin ~/.local/share/nvim/mason/bin|gawk '{print $9}'|sort|uniq -c|gawk '$1>1'
```

## 查看位置

```zsh
gls -l /opt/homebrew/bin ~/software/gopath/bin ~/software/npm/install/bin ~/.local/share/nvim/mason/bin|awk '{print $9}'|sort|uniq -c|awk '$1>1'|awk 'NR>1{print $2}'|xargs -n1 -I{} bash -c 'whereis -a {}'
```

```markdown-runner
npm: /Users/chenxu/software/npm/install/bin/npm /opt/homebrew/bin/npm /Users/chenxu/software/npm/install/share/man/man1/npm.1 /opt/homebrew/share/man/man1/npm.1
npx: /Users/chenxu/software/npm/install/bin/npx /opt/homebrew/bin/npx /Users/chenxu/software/npm/install/share/man/man1/npx.1 /opt/homebrew/share/man/man1/npx.1
```

## 未解决

- [X] `rustfmt` as origin from rust
- [ ] `npm`
- [ ] `npx`
