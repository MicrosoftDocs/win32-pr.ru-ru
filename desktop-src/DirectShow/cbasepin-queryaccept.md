---
description: 'Метод Куерякцепт определяет, принимает ли ПИН-код указанный тип носителя. Этот метод реализует метод Ипин:: Куерякцепт.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Кбасепин. Куерякцепт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669501"
---
# <a name="cbasepinqueryaccept-method"></a>Кбасепин. Куерякцепт, метод

`QueryAccept`Метод определяет, принимает ли ПИН-код указанный тип носителя. Этот метод реализует метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_Если тип мультимедиа является допустимым, возвращается значение ОК. В противном случае возвращает \_ значение S false.

## <a name="remarks"></a>Комментарии

В базовом классе этот метод делегирует методу [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) . Если **чеккмедиатипе** завершается сбоем, `QueryAccept` возвращает \_ значение S false.

Этот метод не удерживает критическую секцию закрепления ([**кбасепин:: m \_ плокк**](cbasepin-m-plock.md)). Если производный класс динамически изменяет набор допустимых типов мультимедиа, следует переопределить этот метод для хранения критической секции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




