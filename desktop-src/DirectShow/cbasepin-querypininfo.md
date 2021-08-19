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
ms.openlocfilehash: 544039b1076848cb796f290ea98aa8aac359b26ebfb64f90a27d316a9d0cc34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823243"
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

## <a name="remarks"></a>Remarks

Этот метод использует переменную-член [**кбасепин:: m \_ pName**](cbasepin-m-pname.md) для элемента **ачнаме** в \_ информационной структуре.

Если метод возвращает значение, если элемент **пфилтер** структуры PIN-кода \_ не **равен null**, то он содержит необработанные ссылки. Не забудьте освободить интерфейс по завершении.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




