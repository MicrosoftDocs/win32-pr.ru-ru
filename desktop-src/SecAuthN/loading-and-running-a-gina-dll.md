---
description: Windows загружает и выполняет стандартную библиотеку DLL Microsoft GINA (MSGina.dll). Чтобы загрузить другую GINA, необходимо изменить значение раздела реестра.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Загрузка и запуск библиотеки DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650838"
---
# <a name="loading-and-running-a-gina-dll"></a>Загрузка и запуск библиотеки DLL GINA

Windows загружает и выполняет стандартную библиотеку DLL Microsoft GINA (MSGina.dll). Чтобы загрузить другую [*GINA*](../secgloss/g-gly.md), необходимо изменить следующее значение раздела реестра:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

Если значение ключа Гинадлл имеется, оно должно содержать имя библиотеки DLL GINA, которая будет загружаться и использоваться [*Winlogon*](../secgloss/w-gly.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание и тестирование библиотеки DLL GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Функции экспорта GINA](authentication-functions.md)
</dt> <dt>

[Структуры GINA](authentication-structures.md)
</dt> <dt>

[Функции GINA служб терминалов](terminal-services-gina-functions.md)
</dt> </dl>

 

 
