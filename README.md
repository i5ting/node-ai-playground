# playground


## 学习

[https://github.com/vercel/ai-chatbot](https://github.com/vercel/ai-chatbot是一个非常好的易于学习的Node.js)

是一个非常好的易于学习的Node.js AI Agent开发项目模版。

1、基于next，ai-sdk，实现基于openai模型的chatbot功能，技术栈和功能很实用。

2、足够小，100个ts文件，代码行数10000行左右，结构清晰，简单易学。

3、前后端，典型的全栈应用，包含postgre db，鉴权，react，ai，非常全面了。很多最佳实践，比如toast库，密码加盐处理等。

4、可以使用aihubmix等openai代理服务，支持支付宝。

5、扩展性强，使用其他模型，以及langchain、llamaindex等。

部署还是有点麻烦，涉及的内容还是比较多的。


本地部署

- 参考文档
- 创建postgres，使用vercel的在线的serverless版postgres。
- 执行本地db初始化和迁移

执行pnpm dev启动，注册用户，然后就可以成功访问了。但大模型用不了

大家都知道openai在国内的情况，

这里采用[aihubmix](https://doc.aihubmix.com/coding/%E5%9C%A8%E5%AE%98%E6%96%B9%20openai%20%E5%BA%93%E4%B8%AD%E4%BD%BF%E7%94%A8)，支付宝付费，基本够用，充个1刀或5刀。


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

