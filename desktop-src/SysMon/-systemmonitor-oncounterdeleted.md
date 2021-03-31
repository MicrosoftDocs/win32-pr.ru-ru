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
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988708"
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

 

 





