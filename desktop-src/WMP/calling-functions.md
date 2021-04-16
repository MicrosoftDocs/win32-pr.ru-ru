---
title: Вызов функций
description: Вызов функций
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Обложки проигрывателя Windows Media, вызов функций в JScript
- обложки, вызов функций в JScript
- вызов функций в JScript
- Файлы JScript для обложек, вызов функций
- Обложки проигрывателя Windows Media, атрибут scriptFile в JScript
- обложки, атрибут scriptFile в JScript
- атрибуты, scriptFile в JScript
- атрибут scriptFile в JScript
- Файлы JScript для обложек, атрибут scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532462"
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
> Если имеется более одного представления, то для кода XML и JScript, выполняемого с текущим представлением, доступны только функции из файлов, загруженных в текущее представление. Файлы, загруженные в другие представления, не находятся в области действия с текущим представлением.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование JScript**](using-jscript.md)
</dt> </dl>

 

 




