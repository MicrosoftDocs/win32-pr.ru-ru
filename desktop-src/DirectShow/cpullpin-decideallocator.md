---
description: Метод ДеЦидеаллокатор согласовывает распределитель с выходным закреплением.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Кпуллпин. ДеЦидеаллокатор, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e02fe78631c6ddee01b7acc96d761f71b80e8d3e1738d2ed6f6ae40d70b0c5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055064"
---
# <a name="cpullpindecideallocator-method"></a>Кпуллпин. ДеЦидеаллокатор, метод

`DecideAllocator`Метод согласовывает распределитель с выходным закреплением.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паллок* 
</dt> <dd>

Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) предпочтительного распределителя входного контакта или **значение NULL**.

</dd> <dt>

*ппропс* 
</dt> <dd>

Указатель на необязательную [**структуру \_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу входного контакта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК, если успешно, или код ошибки в противном случае.

## <a name="remarks"></a>Remarks

Этот метод вызывает метод [**иасинкреадер:: рекуесталлокатор**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) для согласования распределителя. Он передает параметр *паллок* непосредственно в метод **рекуесталлокатор** . Он передает параметр *ппропс* в **Рекуесталлокатор** , если *ппропс* имеет значение, отличное от **null**. в противном случае он создает структуру **\_ свойств распределителя** с запросом по умолчанию из трех буферов размером 64 КБ.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> <dt>

[**кпуллпин:: Подключение**](cpullpin-connect.md)
</dt> </dl>

 

 




