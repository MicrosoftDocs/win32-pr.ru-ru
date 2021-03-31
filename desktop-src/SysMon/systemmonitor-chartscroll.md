---
title: Системмонитор. Чартскролл, свойство
description: Возвращает или задает значение, определяющее, прокручивается ли линейный график в представлении.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Сисмон свойство Чартскролл
- Свойство Чартскролл Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Чартскролл
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988757"
---
# <a name="systemmonitorchartscroll-property"></a>Системмонитор. Чартскролл, свойство

Возвращает или задает значение, определяющее, прокручивается ли линейный график в представлении.

## <a name="syntax"></a>Синтаксис


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Значение свойства

Значение true, если линейный график непрерывно прокручивается справа налево; в противном случае значение false, если линейный график рисуется слева направо и заключает себя в представление. Значение по умолчанию — false.

## <a name="remarks"></a>Комментарии

Это значение игнорируется, если [**системмонитор. дисплайтипе**](systemmonitor-displaytype.md) не [**DisplayTypeConstants.sysмонлинеграф**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



 

 





