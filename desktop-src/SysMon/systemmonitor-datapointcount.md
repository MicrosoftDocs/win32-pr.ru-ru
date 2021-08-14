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
ms.openlocfilehash: 3d7d1212f3f1467c0fb505e84dffdd9cc6bb381c19d8ccc34ad38ee46562ec6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882629"
---
# <a name="systemmonitordatapointcount-property"></a>Системмонитор. Датапоинткаунт, свойство

Возвращает или задает количество точек данных, отображаемых в линейном графе.

## <a name="syntax"></a>Синтаксис


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Значение свойства

Количество точек данных, отображаемых в представлении для линейного графика. Значение по умолчанию — 100 точек данных. Допустимый диапазон значений: от 2 до 1 000.

## <a name="remarks"></a>Remarks

Это свойство используется только в том случае, если [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) является **сисмонкуррентактивити**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



 

 





