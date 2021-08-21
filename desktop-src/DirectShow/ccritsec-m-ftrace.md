---
description: Логическое значение, указывающее, следует ли отслеживать эту блокировку.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Элемент Ккритсек:: m_fTrace (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5a47437e4f9ab475b64979ec970604ac7a621d2ab53ea7a3c87742fa81a8aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074398"
---
# <a name="ccritsecm_ftrace-member"></a>Элемент Ккритсек:: m \_ фтраце

Логическое значение, указывающее, следует ли отслеживать эту блокировку.

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Remarks

Эта переменная-член определена только в отладочной версии базового класса. Если значение равно **true**, трассировка состояния блокировки записывается в журнал отладки. (Журнал отладки для критически важных разделов должен быть активным.) Дополнительные сведения см. в разделе [**дбглокктраце**](dbglocktrace.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

 




