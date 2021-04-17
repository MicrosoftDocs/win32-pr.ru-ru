---
description: Метод Сеттимеадвисе настраивает событие таймера со ссылочным временем.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Ккмдкуеуе. Сеттимеадвисе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674795"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Ккмдкуеуе. Сеттимеадвисе, метод

`SetTimeAdvise`Метод настраивает событие таймера со ссылочным временем.

## <a name="syntax"></a>Синтаксис


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция-член вызывает метод [**иреференцеклокк:: адвисетиме**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) , чтобы настроить уведомление для самого раннего времени, необходимого в очереди. Отложенные команды времени презентации всегда проверяются. Если граф фильтра находится в режиме выполнения, также проверяются отложенные команды, использующие потоковое время.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




