---
description: 'Метод Жеталлокаторрекуирементс извлекает свойства распределителя, запрошенные ПИН-кодом. Этот метод реализует метод Имеминпутпин:: Жеталлокаторрекуирементс.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Ктрансинплацеинпутпин. Жеталлокаторрекуирементс, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676052"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>Ктрансинплацеинпутпин. Жеталлокаторрекуирементс, метод

`GetAllocatorRequirements`Метод получает свойства распределителя, запрошенные ПИН-кодом. Этот метод реализует метод [**имеминпутпин:: жеталлокаторрекуирементс**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .

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

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                               | Описание                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно<br/>                                                                                   |
| <dl> <dt>**E \_ нотимпл**</dt> </dl> | Выходной ПИН-код не подключен, или его входной ПИН-код не поддерживает метод.<br/> |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя<br/>                                                                 |



 

## <a name="remarks"></a>Комментарии

Если выходной ПИН-код подключен, этот метод передает вызов нисходящего входного ПИН-кода. В противном случае возвращается E \_ нотимпл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацеинпутпин**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




