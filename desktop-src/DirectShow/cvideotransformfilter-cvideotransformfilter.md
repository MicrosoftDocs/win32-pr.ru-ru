---
description: Метод конструктора Квидеотрансформфилтер. Квидеотрансформфилтер.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Конструктор Квидеотрансформфилтер. Квидеотрансформфилтер (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1db2b665a1525f1352844a2963bd44a761a080a058154419b3320f7113aa3740
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086884"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a>Квидеотрансформфилтер. Квидеотрансформфилтер, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Строка, содержащая имя отладки фильтра. Дополнительные сведения см. в разделе [**кбасеобжект:: кбасеобжект**](cbaseobject-cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*этому* 
</dt> <dd>

Идентификатор класса фильтра.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>втранс. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




