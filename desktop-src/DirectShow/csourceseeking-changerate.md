---
description: Метод Чанжерате вызывается при изменении скорости воспроизведения.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Ксаурцесикинг. Чанжерате, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685264"
---
# <a name="csourceseekingchangerate-method"></a>Ксаурцесикинг. Чанжерате, метод

`ChangeRate`Метод вызывается при изменении скорости воспроизведения.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Метод [**ксаурцесикинг:: сетрате**](csourceseeking-setrate.md) вызывает этот метод, который должен реализовываться производным классом. Метод **сетрате** обновляет переменную члена [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) , но не проверяет новое значение. Нулевую скорость следует всегда отклонять. Ставки меньше нуля указывают на отрицательное воспроизведение. Большинство фильтров не поддерживает отрицательные тарифы.

В следующем примере показана возможная реализация:


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
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

 

 




