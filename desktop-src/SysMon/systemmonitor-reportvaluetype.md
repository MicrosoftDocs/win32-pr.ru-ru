---
title: Системмонитор. Репортвалуетипе, свойство
description: Возвращает или задает значение, определяющее, отображает ли гистограмма и представления отчетов Последнее значение, заданное в интервале выборки, или вычисленное значение из выборки, например среднее или минимальное значение счетчика.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Сисмон свойство Репортвалуетипе
- Репортвалуетипе Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Репортвалуетипе
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988613"
---
# <a name="systemmonitorreportvaluetype-property"></a>Системмонитор. Репортвалуетипе, свойство

Возвращает или задает значение, определяющее, отображает ли гистограмма и представления отчетов Последнее значение, заданное в интервале выборки, или вычисленное значение из выборки, например среднее или минимальное значение счетчика.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Значение свойства

Определяет, отображает ли гистограмма и представления отчетов Последнее значение, выборка которого производилось в интервале выборки, или вычисленное значение из интервала выборки. Возможные значения см. в разделе [**репортвалуетипеконстантс**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Комментарии

СИСМОН игнорирует это значение и использует [**ReportValueTypeConstants.sysмондефаултвалуе**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) , если [**системмонитор. Дисплайтипе**](systemmonitor-displaytype.md) не [**DisplayTypeConstants.sysмонхистограм**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) или **DisplayTypeConstants.sysмонрепорт**.

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

 

 





