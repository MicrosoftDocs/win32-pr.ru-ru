---
description: Метод Чанжестарт вызывается при изменении начальной координаты.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Ксаурцесикинг. Чанжестарт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f7c0d9a86d33d13c95295c5ef1ef46a3e6c02371d1b6520572750450320b1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073368"
---
# <a name="csourceseekingchangestart-method"></a>Ксаурцесикинг. Чанжестарт, метод

`ChangeStart`Метод вызывается при изменении начальной должности.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Метод [**ксаурцесикинг:: сетпоситионс**](csourceseeking-setpositions.md) вызывает этот метод при изменении начальной должности. Этот метод является чисто виртуальным; производный класс должен реализовать его. После операции поиска штампы времени должны перезапускаться с нуля. Время работы с носителями должно соответствовать новому времени начала. В следующем примере показана возможная реализация:


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




