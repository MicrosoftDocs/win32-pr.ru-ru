---
description: Метод Сетконфигинфо задает указатель Играфконфиг и событие завершения.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Кдинамикаутпутпин. Сетконфигинфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23b492eaf4b5f712a51132eefcceac12a772b17b8285d8c6edb1a6cec268b1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074238"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Кдинамикаутпутпин. Сетконфигинфо, метод

`SetConfigInfo`Метод задает указатель [**играфконфиг**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) и событие завершения.

## <a name="syntax"></a>Синтаксис


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пграфконфиг* 
</dt> <dd>

Указатель на интерфейс [**играфконфиг**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) или **значение NULL**.

</dd> <dt>

*хстопевент* 
</dt> <dd>

Дескриптор события, сигнального при остановке фильтра, или **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Фильтр должен вызвать этот метод при соединении графа фильтра. Диспетчер графов фильтров поддерживает **играфконфиг**. Для параметра *хстопевент* Создайте событие ручного сброса. Когда фильтр покидает граф фильтра, вызовите этот метод еще раз с **нулевым значением** для обоих параметров.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




