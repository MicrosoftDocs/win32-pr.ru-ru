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
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657961"
---
# <a name="ccritsecm_ftrace-member"></a>Элемент Ккритсек:: m \_ фтраце

Логическое значение, указывающее, следует ли отслеживать эту блокировку.

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Примечания

Эта переменная-член определена только в отладочной версии базового класса. Если значение равно **true**, трассировка состояния блокировки записывается в журнал отладки. (Журнал отладки для критически важных разделов должен быть активным.) Дополнительные сведения см. в разделе [**дбглокктраце**](dbglocktrace.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

 




