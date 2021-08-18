---
description: Включает содержимое одного MOF-файла в другой MOF-файл.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b7577639bd215fc051c2f1303e74fe946341a31c4b6708f881c3c9fabae2372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557781"
---
# <a name="include"></a>"#include"
/* Заголовок: Мимоф. mof                           *//*   Title: MyMof2. mof */

\#Команда "включить препроцессор" включает содержимое одного MOF-файла в другой MOF-файл. В следующем примере кода описывается синтаксис \# команды include.

``` syntax
#include ("Moffile.mof")
```

В предыдущем примере Моффиле. MOF — это имя MOF-файла, который необходимо включить.

В следующем примере показаны два MOF-файла. При компиляции первого файла MOF компилятор автоматически компилирует второй MOF-файл (Mymof2. MOF) в месте, где размещена \# Инструкция include.

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

В предыдущий пример включен следующий MOF-файл:

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Команды препроцессора](preprocessor-commands.md)
</dt> </dl>

 

 



