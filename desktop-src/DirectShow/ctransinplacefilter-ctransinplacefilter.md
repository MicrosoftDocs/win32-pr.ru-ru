---
description: Метод конструктора Ктрансинплацефилтер. Ктрансинплацефилтер.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Конструктор Ктрансинплацефилтер. Ктрансинплацефилтер (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98fb678a2df7c79e40c5ecf39b0a059ebc9e44f4f3f603e1d1a6551446204aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767584"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>Ктрансинплацефилтер. Ктрансинплацефилтер, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побжектнаме* 
</dt> <dd>

Строка, содержащая имя отладки фильтра. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

</dd> <dt>

*лпунк* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*этому* 
</dt> <dd>

Идентификатор класса фильтра.

</dd> <dt>

*фр* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*бмодифиесдата* 
</dt> <dd>

Логическое значение, указывающее, изменяет ли фильтр входные данные. **Значение true** показывает, что фильтр изменяет данные. В противном случае фильтр передает неизмененные данные.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




