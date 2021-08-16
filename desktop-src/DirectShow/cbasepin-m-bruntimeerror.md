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
ms.openlocfilehash: ffc07a15f7c34744be52c5e2c7b5233e1885b58c5b9b7d078871277f8fc0efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823336"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Элемент Кбасепин:: m \_ брунтимиррор

Флаг, указывающий, произошла ли ошибка во время выполнения.

## <a name="syntax"></a>Синтаксис


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Remarks

По умолчанию этот флаг **имеет значение false**. Установите для флага **значение true** , если во время потоковой передачи возникает ошибка во время выполнения. Метод [**кбасепин:: Inactive**](cbasepin-inactive.md) сбрасывает флаг в **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




