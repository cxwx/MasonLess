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
```shell
ls -l /opt/homebrew/bin ~/.local/share/nvim/mason/bin|awk '{print $11}'|sort|uniq -c|awk '$1>1'
```


```shell
ls -l /opt/homebrew/bin ~/.local/share/nvim/mason/bin|awk '{print $11}'|sort|uniq -c|awk '$1>1'|awk 'NR>1{print $2}'|xargs -n1 -I{} bash -c 'whereis -a {}'
```
