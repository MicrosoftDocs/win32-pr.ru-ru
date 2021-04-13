---
title: донотаддаллаппликатионпаккажесторестриктионс
description: Определяет, будут ли вызовы RPC автоматически добавлять \_ \_ идентификаторы безопасности пакетов всех приложений в ограничения com по умолчанию.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410676"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>донотаддаллаппликатионпаккажесторестриктионс

Определяет, будут ли вызовы RPC автоматически добавлять \_ \_ идентификаторы безопасности пакетов всех приложений в ограничения com по умолчанию.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ DWORD** .



| Значение | Описание                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Отключает приложения Магазина Windows при миграции с Windows 7 на Windows 8.                   |
| 1     | Не добавляет \_ идентификатор безопасности "все \_ пакеты приложений" в ограничения com. Это значение по умолчанию. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




