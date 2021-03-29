---
description: 'Метод Skip пропускает указанное число типов мультимедиа. Этот метод реализует метод Иенуммедиатипес:: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Метод Ценуммедиатипес. Skip (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657588"
---
# <a name="cenummediatypesskip-method"></a>Ценуммедиатипес. Skip, метод

`Skip`Метод пропускает указанное число типов мультимедиа. Этот метод реализует метод [**иенуммедиатипес:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кмедиатипес* 
</dt> <dd>

Число пропускаемых типов мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                                | Описание                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Пропущено после конца последовательности.<br/>                                    |
| <dl> <dt>**\_ОК**</dt> </dl>                       | Успешно.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt> </dl> | Состояние ПИН-кода изменилось и теперь не согласуется с перечислителем.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ценуммедиатипес**](cenummediatypes.md)
</dt> </dl>

 

 




