# @lpenser/git-clone

从git存储库（GitHub，GitLab，Bitbucket）下载代码到指定目录，支持async，await

## Installation

npm install @lpenser/git-clone

# API

### download(repository, destination, options, callback)

# Examples

```
import  download  from '@lpenser/git-clone';
import * as ora  from 'ora';

export default async function downloadTemplate(template, templateDir) {
    const spinner = ora('正在初始化项目').start();
    await download(template, templateDir,{}, async function (err) {
        await  spinner.stop();
        if (err) {
            console.log('Failed to download repo ' + template + ': ' + err.message.trim());
        }
      })
}

```
