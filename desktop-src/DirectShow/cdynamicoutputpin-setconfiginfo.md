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
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657231"
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

## <a name="remarks"></a>Комментарии

Фильтр должен вызвать этот метод при соединении графа фильтра. Диспетчер графов фильтров поддерживает **играфконфиг**. Для параметра *хстопевент* Создайте событие ручного сброса. Когда фильтр покидает граф фильтра, вызовите этот метод еще раз с **нулевым значением** для обоих параметров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




