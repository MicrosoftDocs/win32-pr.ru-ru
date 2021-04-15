---
description: Метод SetProperties задает количество выделяемых буферов и размер каждого буфера.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Кмемаллокатор. SetProperties, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675666"
---
# <a name="cmemallocatorsetproperties-method"></a>Кмемаллокатор. SetProperties, метод

`SetProperties`Метод задает количество выделяемых буферов и размер каждого буфера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*предпоручение* 
</dt> <dd>

Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу.

</dd> <dt>

*пактуал* 
</dt> <dd>

Указатель на структуру **\_ свойств распределителя** , которая получает фактические свойства буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                                 | Описание                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                        | Успешно.<br/>                                                   |
| <dl> <dt>**\_указатель E**</dt> </dl>                   | **Пустой** аргумент указателя.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ уже \_ зафиксирован**</dt> </dl>   | Невозможно изменить выделенную память, пока фильтр активен.<br/> |
| <dl> <dt>**VFW \_ E \_ бадалигн**</dt> </dl>             | Указано недопустимое выравнивание.<br/>                        |
| <dl> <dt>**\_ \_ необработанных буферов VFW E \_**</dt> </dl> | Один или несколько буферов все еще активны.<br/>                      |



 

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) .

Выравнивание буфера, заданное элементом **кбалигн** структуры **\_ свойств распределителя** , должно быть четной степенью двух.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




