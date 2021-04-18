---
description: Флаг, указывающий, произошла ли ошибка во время выполнения.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Элемент Кбасепин:: m_bRunTimeError (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657975"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Элемент Кбасепин:: m \_ брунтимиррор

Флаг, указывающий, произошла ли ошибка во время выполнения.

## <a name="syntax"></a>Синтаксис


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Примечания

По умолчанию этот флаг **имеет значение false**. Установите для флага **значение true** , если во время потоковой передачи возникает ошибка во время выполнения. Метод [**кбасепин:: Inactive**](cbasepin-inactive.md) сбрасывает флаг в **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




