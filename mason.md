<!-- *********************************************************************** -->
<!--                                                                         -->
<!--                                                      :::      ::::::::  -->
<!-- mason.md                                           :+:      :+:    :+:  -->
<!--                                                  +:+ +:+         +:+    -->
<!-- By: chenxu <chenxu@mail.ustc.edu.cn>           +#+  +:+       +#+       -->
<!--                                              +#+#+#+#+#+   +#+          -->
<!-- Created: 2024/11/29 16:00:26 by chenxu            #+#    #+#            -->
<!-- Updated: 2024/11/30 20:55:09 by chenxu           ###   ########.fr      -->
<!--                                                                         -->
<!-- *********************************************************************** -->
<!-- cspell:disable -->
```shell
ls -l /opt/homebrew/bin ~/.local/share/nvim/mason/bin|awk '{print $11}'|sort|uniq -c|awk '$1>1'
```

```shell
for file in `cat aa|awk '{print $2}'`
do
  echo $file
  whereis -a $file
done

```

```shell
ls -l /opt/homebrew/bin ~/.local/share/nvim/mason/bin|awk '{print $11}'|sort|uniq -c|awk '$1>1'|awk 'NR>1{print $2}'|xargs -n1 -I{} bash -c 'whereis -a {}'
```
