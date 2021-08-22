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
ms.openlocfilehash: 57b085cd82c45fd78ddaa4794084cba775e1c80cd8b9e3b8df4c9680379ba462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586374"
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

## <a name="remarks"></a>Remarks

Когда закрепление вывода инициализирует распределитель памяти, он может вызвать этот метод, чтобы определить, имеет ли входной ПИН-код требования к буферу. Дополнительные сведения см. в разделе [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md).

Реализация этого метода является необязательной. Если фильтр имеет особые требования выравнивания или префикса, Переопределите этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




