---
description: Метод Жеталлокаторрекуирементс извлекает свойства распределителя, запрашиваемые входным закреплением.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Кбасеинпутпин. Жеталлокаторрекуирементс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657065"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>Кбасеинпутпин. Жеталлокаторрекуирементс, метод

`GetAllocatorRequirements`Метод получает свойства распределителя, запрашиваемые входным закреплением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппропс* 
</dt> <dd>

Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая заполняется требованиями.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ нотимпл.

## <a name="remarks"></a>Комментарии

Когда закрепление вывода инициализирует распределитель памяти, он может вызвать этот метод, чтобы определить, имеет ли входной ПИН-код требования к буферу. Дополнительные сведения см. в разделе [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md).

Реализация этого метода является необязательной. Если фильтр имеет особые требования выравнивания или префикса, Переопределите этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




