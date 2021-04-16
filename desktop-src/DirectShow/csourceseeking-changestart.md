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
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658032"
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

## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




