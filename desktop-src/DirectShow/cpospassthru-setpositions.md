---
description: 'Кпоспасссру. Сетпоситионс, метод Сетпоситионс задает текущее расположение и точку окончания. Этот метод реализует метод Имедиасикинг:: Сетпоситионс.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Кпоспасссру. Сетпоситионс, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d5ed5a25c5ceb4cbe96571ef83945fdf5edd1bbd373de875f7339c13c1b43dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909194"
---
# <a name="cpospassthrusetpositions-method"></a>Кпоспасссру. Сетпоситионс, метод

`SetPositions`Метод задает текущее расположение и точку окончания. Этот метод реализует метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуррент* 
</dt> <dd>

Указатель на переменную, указывающую текущее расположение в единицах текущего формата времени.

</dd> <dt>

*двкуррентфлагс* 
</dt> <dd>

Побитовое сочетание флагов. Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> <dt>

*пстоп* 
</dt> <dd>

Указатель на переменную, задающую время окончания в единицах текущего формата времени.

</dd> <dt>

*двстопфлагс* 
</dt> <dd>

Побитовое сочетание флагов. Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




