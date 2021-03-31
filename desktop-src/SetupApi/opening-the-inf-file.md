---
description: Необходимо использовать функцию Сетупопенинффиле, чтобы открыть INF-файл, прежде чем можно будет получить из него сведения или добавить в него другие INF-файлы.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Открытие INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910336"
---
# <a name="opening-the-inf-file"></a>Открытие INF-файла

Необходимо использовать функцию [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) , чтобы открыть INF-файл, прежде чем можно будет получить из него сведения или добавить в него другие INF-файлы.

Следующий командлет открывает INF-файл с помощью [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) и возвращает маркер минф в открытый файл INF. Параметр *инфкласс* параметра **Сетупопенинффиле** указывается как **null** , чтобы указать, что класс INF-файла должен игнорироваться.


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



После открытия файла INF можно вызвать функцию [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , чтобы добавить файл в открытый INF-файл. Чтобы добавить несколько файлов, повторите эту процедуру. Если вызвать функцию **сетупопенаппендинффиле** и переданное в нее имя файла имеет **значение NULL**, функция выполнит поиск в разделе версии открытого INF-файла (и всех добавленных INF-файлов) для ключа лайаутфиле. Если функция находит ключ, она добавляет файл, заданный этим ключом (обычно макет. INF). Если несколько файлов INF объединены, **сетупопенаппендинффиле** начинает с последнего ДОБАВЛЕНного INF-файла при поиске раздела версии.

 

 



