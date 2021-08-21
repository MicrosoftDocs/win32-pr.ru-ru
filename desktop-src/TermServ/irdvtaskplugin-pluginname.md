---
title: Свойство PluginName Ирдвтаскплугин (Тспубплугинком. h)
description: Содержит отображаемое имя агента задач.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства PluginName
- Службы удаленных рабочих столов свойства PluginName, интерфейс Ирдвтаскплугин
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугин, свойство PluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129335"
---
# <a name="irdvtaskpluginpluginname-property"></a>Ирдвтаскплугин: свойство Лугиннаме:P

Содержит отображаемое имя агента задач. Это имя используется только в целях ведения журнала.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Отображаемое имя агента задачи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Тспубплугинком. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ирдвтаскплугин**](irdvtaskplugin.md)
</dt> </dl>

 

 





