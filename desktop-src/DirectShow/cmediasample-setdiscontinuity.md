---
description: 'Метод Сетдисконтинуити указывает, представляет ли этот образец разрыв в потоке данных. Этот метод реализует метод Имедиасампле:: Сетдисконтинуити.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Кмедиасампле. Сетдисконтинуити, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4189498c60a52692c057a867dba8bc48c43d2b1c32fbd6091738a3711102f4b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832184"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>Кмедиасампле. Сетдисконтинуити, метод

`SetDiscontinuity`Метод указывает, представляет ли этот образец разрыв в потоке данных. Этот метод реализует метод [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бдисконт* 
</dt> <dd>

Логическое значение, указывающее, является ли этот пример ненепрерывным. Если **значение — true**, пример носителя не помещается в предыдущий пример.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод обновляет переменную члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает свойство ненепрерывности.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




