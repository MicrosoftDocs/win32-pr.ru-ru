---
title: донотаддаллаппликатионпаккажесторестриктионс
description: Определяет, будут ли вызовы RPC автоматически добавлять \_ \_ идентификаторы безопасности пакетов всех приложений в ограничения com по умолчанию.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1608d49d7e5bebc977ace8e59e4b31c5b13da8ab4f743e89095b9f31632453c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737010"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>донотаддаллаппликатионпаккажесторестриктионс

Определяет, будут ли вызовы RPC автоматически добавлять \_ \_ идентификаторы безопасности пакетов всех приложений в ограничения com по умолчанию.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ DWORD** .



| Значение | Описание                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | отключает Windows приложения магазина при миграции с Windows 7 на Windows 8.                   |
| 1     | Не добавляет \_ идентификатор безопасности "все \_ пакеты приложений" в ограничения com. Это значение по умолчанию. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




