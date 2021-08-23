---
title: Системмонитор. Онкаунтерделетед, событие
description: Уведомляет вас перед удалением счетчика из коллекции счетчиков.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Сисмон события Онкаунтерделетед
- Онкаунтерделетед Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Онкаунтерделетед
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c178cb0b9c19fde0814f15729ffd49a0a0dbea65023bde06673cd843aeb668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884006"
---
# <a name="systemmonitoroncounterdeleted-event"></a>Системмонитор. Онкаунтерделетед, событие

Уведомляет вас перед удалением счетчика из коллекции [**счетчиков**](counters.md) .

## <a name="syntax"></a>Синтаксис


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Индекс удаляемого счетчика из объекта коллекции [**счетчиков**](counters.md) .

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

[**Системмонитор. Онкаунтераддед**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**Системмонитор. Онкаунтерселектед**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





