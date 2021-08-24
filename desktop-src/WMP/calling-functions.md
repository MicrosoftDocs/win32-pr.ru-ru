---
title: Вызов функций
description: Вызов функций
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- обложки проигрыватель Windows Media, вызов функций в JScript
- обложки, вызов функций в JScript
- вызов функций в JScript
- JScript файлы для обложек, вызов функций
- проигрыватель Windows Media обложек, атрибут scriptFile в JScript
- обложки, атрибут scriptFile в JScript
- атрибуты, scriptFile в JScript
- атрибут scriptFile в JScript
- JScript файлы для обложек, атрибут scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e41b5fdfd6109292a1a42cae43e42e8424348090541fd50a8d83f04d23b8329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764274"
---
# <a name="calling-functions"></a>Вызов функций

Если необходимо вызвать более нескольких строк кода, можно загрузить файл скрипта с помощью атрибута **scriptFile** элемента **View** и вызвать функции в скрипте. В одном представлении можно загрузить несколько файлов:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



После загрузки файлов скриптов можно вызывать в них функции из раздела представления. Например, чтобы вызвать функцию с именем *MyFunction* при нажатии на нечто, введите следующее:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> при наличии нескольких представлений доступны только функции в файлах, загруженных в текущее представление, и JScript код, выполняемый с текущим представлением. Файлы, загруженные в другие представления, не находятся в области действия с текущим представлением.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Использование JScript**](using-jscript.md)
</dt> </dl>

 

 




