# playground


## 学习

https://github.com/vercel/ai-chatbot

这个项目代码质量还不错。

本地部署

- 参考文档
- 创建postgres，使用vercel的在线的serverless版postgres。
- 执行本地db初始化和迁移

执行pnpm dev启动，注册用户，然后就可以成功访问了。但大模型用不了

大家都知道openai在国内的情况，

这里采用https://doc.aihubmix.com/coding/%E5%9C%A8%E5%AE%98%E6%96%B9%20openai%20%E5%BA%93%E4%B8%AD%E4%BD%BF%E7%94%A8，支付宝付费，基本够用，充个1刀或5刀。


原@ai-sdk/openai里的openai方法，没有baseURL的。

```
import { openai } from '@ai-sdk/openai';
```

略改造。

```
import { createOpenAI } from '@ai-sdk/openai';

const openai = createOpenAI({
  // custom settings, e.g.
  compatibility: "strict", // strict mode, enable when using the OpenAI API
  apiKey: process.env.OPENAI_API_KEY,
  baseURL: process.env.OPENAI_BASE_URL,
});
```

执行pnpm dev启动，此时就是一个完全的

![![](20250212092002.png)](imgs/20250212092116.png)

## 从LlamaIndexTs学习


## other


### 在md里粘贴图片

安装https://marketplace.visualstudio.com/items?itemName=telesoho.vscode-markdown-paste-image扩展，用于在md里粘贴图片

快捷键alt + cmd + v。

