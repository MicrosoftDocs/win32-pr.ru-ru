---
description: Windows загружает и выполняет стандартную библиотеку DLL Microsoft GINA (MSGina.dll). Чтобы загрузить другую GINA, необходимо изменить значение раздела реестра.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Загрузка и запуск библиотеки DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140957"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание и тестирование библиотеки DLL GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Функции экспорта GINA](authentication-functions.md)
</dt> <dt>

[Структуры GINA](authentication-structures.md)
</dt> <dt>

[Функции GINA служб терминалов](terminal-services-gina-functions.md)
</dt> </dl>

 

 
