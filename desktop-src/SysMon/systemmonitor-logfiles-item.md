---
title: Файл_журнала. Item, свойство
description: Извлекает указанный экземпляр Логфилеитем из коллекции.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Свойство элемента Сисмон
- Свойство Item Сисмон, класс LogFile
- Файл_журнала класса Сисмон, свойство Item
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071356"
---
# <a name="logfilesitem-property"></a>Файл_журнала. Item, свойство

Извлекает указанный экземпляр [**логфилеитем**](logfileitem.md) из коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Значение свойства

Экземпляр [**логфилеитем**](logfileitem.md) , соответствующий указанному значению индекса.

## <a name="remarks"></a>Комментарии

Это свойство по умолчанию для объекта [**файл_журнала**](systemmonitor-logfiles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**логфилеитем**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





