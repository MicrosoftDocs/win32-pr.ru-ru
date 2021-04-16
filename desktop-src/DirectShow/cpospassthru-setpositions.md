---
description: 'Метод Сетпоситионс задает текущую и заданную позиции. Этот метод реализует метод Имедиасикинг:: Сетпоситионс.'
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
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658014"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




