---
title: Системмонитор. Онкаунтерселектед, событие
description: Уведомляет вас о том, что выбран счетчик.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Сисмон события Онкаунтерселектед
- Онкаунтерселектед Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Онкаунтерселектед
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e5402eb123c5edd44a5616b6973940ba065e2b0c8c2bfa63e7d151ae30124
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957251"
---
# <a name="systemmonitoroncounterselected-event"></a>Системмонитор. Онкаунтерселектед, событие

Уведомляет вас о том, что выбран счетчик.

## <a name="syntax"></a>Синтаксис


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Индекс выбранного счетчика в объекте коллекции [**счетчиков**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Это событие можно получить, когда

-   Вы устанавливаете [**каунтеритем. Selected**](counteritem-selected.md) в значение true.
-   Пользователь выбирает счетчик в условных обозначениях
-   Пользователь дважды щелкает счетчик в условных обозначениях

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Системмонитор. Онкаунтераддед**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**Системмонитор. Онкаунтерделетед**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





