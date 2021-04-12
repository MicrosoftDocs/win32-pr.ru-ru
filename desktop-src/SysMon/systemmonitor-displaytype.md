---
title: Системмонитор. Дисплайтипе, свойство
description: Возвращает или задает тип графа, используемый для отображения данных счетчика производительности.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Сисмон свойство Дисплайтипе
- Дисплайтипе Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Дисплайтипе
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136002"
---
# <a name="systemmonitordisplaytype-property"></a>Системмонитор. Дисплайтипе, свойство

Возвращает или задает тип графа, используемый для отображения данных счетчика производительности.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>Значение свойства

Тип графа, используемый для отображения данных счетчика производительности. Возможные значения см. в разделе [**дисплайтипеконстантс**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="exceptions"></a>Исключения



| Тип исключения               | Условие                                         |
|------------------------------|---------------------------------------------------|
| **System. ArgumentException** | Указано недопустимое значение диаграммы или отчета. |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> </dl>

 

 





