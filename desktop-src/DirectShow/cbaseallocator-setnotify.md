---
description: 'Метод Сетнотифи задает или удаляет обратный вызов для распределителя. Распределитель вызывает метод обратного вызова при вызове метода распределителя Имемаллокатор:: Релеасебуффер.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Кбасеаллокатор. Сетнотифи, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657850"
---
# <a name="cbaseallocatorsetnotify-method"></a>Кбасеаллокатор. Сетнотифи, метод

\[[**Сетнотифи**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) может быть изменен или недоступен в последующих версиях.\]

`SetNotify`Метод задает или удаляет обратный вызов для распределителя. Распределитель вызывает метод обратного вызова при вызове метода распределителя [**имемаллокатор:: релеасебуффер**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнотифи* 
</dt> <dd>

Указатель на интерфейс [**имемаллокаторнотификаллбакктемп**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) , который будет использоваться для обратного вызова. Вызывающий объект должен реализовать интерфейс. Чтобы удалить обратный вызов, используйте значение **null** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод реализует метод [**имемаллокаторкаллбакктемп:: сетнотифи**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) . Распределитель не предоставляет интерфейс [**имемаллокаторкаллбакктемп**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , если в конструкторе [**кбасеаллокатор**](cbaseallocator.md) для флага *Фенаблерелеасекаллбакк* не задано **значение true** .

Этот метод задает переменную члена [**кбасеаллокатор:: m \_ пнотифи**](cbaseallocator-m-pnotify.md) равную *пнотифи* и увеличивает счетчик ссылок в интерфейсе. Если *значение \_ m Пнотифи* не **равно NULL**, метод **Релеасебуффер** распределителя вызывает [**имемаллокаторнотификаллбакктемп:: нотифирелеасе**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease). Сведения о реализации обратного вызова см. в подразделе "Примечания" этого метода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




