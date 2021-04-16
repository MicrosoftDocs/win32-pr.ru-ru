---
description: Метод конструктора.
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
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657981"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




