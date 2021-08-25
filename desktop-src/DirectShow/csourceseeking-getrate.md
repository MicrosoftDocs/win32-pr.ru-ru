---
description: 'Ксаурцесикинг. метод Rate — метод метода Rate извлекает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Rate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Метод Ксаурцесикинг. rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b734a5fafba9e38abbe853a8f3592a212130bf9a68de0efe7125aeea0ea01b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083954"
---
# <a name="csourceseekinggetrate-method"></a>Ксаурцесикинг. метод Rate

`GetRate`Метод получает скорость воспроизведения. Этот метод реализует метод [**имедиасикинг:: Rate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдрате* 
</dt> <dd>

Указатель на переменную, которая получает скорость воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.



| Код возврата                                                                               | Описание                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl> | Значение указателя **null**<br/> |



 

## <a name="remarks"></a>Remarks

Скорость воспроизведения задается переменной-членом [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




