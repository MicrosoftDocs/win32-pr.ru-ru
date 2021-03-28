---
description: Показывает, какой раздел реестра должен быть настроен для предотвращения автозапуска.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Как предотвратить автозапуск для компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985425"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Как предотвратить автозапуск для компонента

Показывает, какой раздел реестра должен быть настроен для предотвращения автозапуска.

## <a name="instructions"></a>Инструкции


Чтобы предотвратить запуск автозапуска в ответ на событие, добавьте следующее значение **reg \_ SZ** , как показано в этом примере.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

Значение является идентификатором класса (CLSID), который компонент, создающий событие, известен в таблице текущих объектов (ROT). Значение не содержит данных.

> [!IMPORTANT]
> В этом ключе идентификаторы CLSID не заключаются в фигурные скобки ( {} ).

 

 

 



