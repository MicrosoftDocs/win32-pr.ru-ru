---
description: 'Метод Куерипининфо извлекает сведения о ПИН-коде. Этот метод реализует метод Ипин:: Куерипининфо.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Кбасепин. Куерипининфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668543"
---
# <a name="cbasepinquerypininfo-method"></a>Кбасепин. Куерипининфо, метод

`QueryPinInfo`Метод получает сведения о ПИН-коде. Этот метод реализует метод [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* 
</dt> <dd>

Указатель на [**\_ информационную структуру ПИН-**](/windows/win32/api/strmif/ns-strmif-pin_info) кода, который получает сведения о ПИН-коде.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="remarks"></a>Комментарии

Этот метод использует переменную-член [**кбасепин:: m \_ pName**](cbasepin-m-pname.md) для элемента **ачнаме** в \_ информационной структуре.

Если метод возвращает значение, если элемент **пфилтер** структуры PIN-кода \_ не **равен null**, то он содержит необработанные ссылки. Не забудьте освободить интерфейс по завершении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




