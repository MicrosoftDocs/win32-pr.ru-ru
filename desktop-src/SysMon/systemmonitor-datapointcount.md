---
title: Системмонитор. Датапоинткаунт, свойство
description: Возвращает или задает количество точек данных, отображаемых в линейном графе.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Сисмон свойство Датапоинткаунт
- Свойство Датапоинткаунт Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Датапоинткаунт
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988426"
---
# <a name="systemmonitordatapointcount-property"></a>Системмонитор. Датапоинткаунт, свойство

Возвращает или задает количество точек данных, отображаемых в линейном графе.

## <a name="syntax"></a>Синтаксис


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Значение свойства

Количество точек данных, отображаемых в представлении для линейного графика. Значение по умолчанию — 100 точек данных. Допустимый диапазон значений: от 2 до 1 000.

## <a name="remarks"></a>Комментарии

Это свойство используется только в том случае, если [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) является **сисмонкуррентактивити**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



 

 





