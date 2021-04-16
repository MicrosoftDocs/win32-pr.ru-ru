---
description: Метод ДеЦидебуфферсизе задает требования к буферу.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Кбасеаутпутпин. ДеЦидебуфферсизе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657889"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>Кбасеаутпутпин. ДеЦидебуфферсизе, метод

`DecideBufferSize`Метод задает требования к буферу.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паллок* 
</dt> <dd>

Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.

</dd> <dt>

*ппропинпутрекуест* 
</dt> <dd>

Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу входного контакта. Если у входного контакта нет каких-либо требований, вызывающий объект должен обнулить члены этой структуры перед вызовом метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.

## <a name="remarks"></a>Комментарии

Переопределите этот метод в производном классе. Вызовите метод [**имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , чтобы указать требования к буферу. Как правило, производный класс будет учитывать требования к буферу входного контакта, но это не обязательно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




