---
title: Системмонитор. Жетлогвиевранже, метод
description: Возвращает дату начала, используемую для получения значений счетчика из файлов журнала.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Метод Жетлогвиевранже Сисмон
- Метод Жетлогвиевранже Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Жетлогвиевранже
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534184"
---
# <a name="systemmonitorgetlogviewrange-method"></a>Системмонитор. Жетлогвиевранже, метод

Возвращает дату начала, используемую для получения значений счетчика из файлов журнала.

## <a name="syntax"></a>Синтаксис


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

Время *начала* \[ заполняет\]
</dt> <dd>

Дата начала, используемая для получения значений счетчиков из файлов журнала.

</dd> <dt>

*StopTime* \[ заполняет\]
</dt> <dd>

Дата окончания, используемая для получения значений счетчика из файлов журнала.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

СИСМОН получает значения счетчиков из файлов журнала, которые находятся в пределах даты начала и окончания, включительно.

Использование этого метода аналогично доступу к свойствам [**системмонитор. логвиевстарт**](systemmonitor-logviewstart.md) и [**системмонитор. логвиевстоп**](systemmonitor-logviewstop.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> <dt>

[**Системмонитор. Сетлогвиевранже**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





