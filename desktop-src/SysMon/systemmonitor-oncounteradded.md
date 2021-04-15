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
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661888"
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Системмонитор. Онкаунтерделетед**](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[**Системмонитор. Онкаунтерселектед**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





