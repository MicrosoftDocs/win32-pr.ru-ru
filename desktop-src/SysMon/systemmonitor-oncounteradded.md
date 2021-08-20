---
title: Системмонитор. Онкаунтераддед, событие
description: Уведомляет о добавлении счетчика в коллекцию счетчиков.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Сисмон события Онкаунтераддед
- Онкаунтераддед Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Онкаунтераддед
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b07837fd3940b9617b9a5f2aa769188f01e00bebcfd2f2cdab5d98bdbdb1abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955110"
---
# <a name="systemmonitoroncounteradded-event"></a>Системмонитор. Онкаунтераддед, событие

Уведомляет о добавлении счетчика в коллекцию [**счетчиков**](counters.md) .

## <a name="syntax"></a>Синтаксис


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Индекс счетчика, добавленного в объект коллекции [**Counters**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Системмонитор. Онкаунтерделетед**](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[**Системмонитор. Онкаунтерселектед**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





