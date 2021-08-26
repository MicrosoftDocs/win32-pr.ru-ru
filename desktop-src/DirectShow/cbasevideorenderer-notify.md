---
description: Метод notify получает уведомление о том, что запрошено изменение качества.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Метод Кбасевидеорендерер. notify (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052194"
---
# <a name="cbasevideorenderernotify-method"></a>Кбасевидеорендерер. notify, метод

`Notify`Метод получает уведомление о том, что запрошено изменение качества.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пселф* \[ окне\]
</dt> <dd>

Указатель на фильтр, отправляющий уведомление.

</dd> <dt>

*вопросы* \[ в\]
</dt> <dd>

Структура уведомления об изменении качества.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) в модуле подготовки видео. Этот метод вызывается, как правило, диспетчером графа фильтров, когда необходимо вырезать качество. Это может произойти, когда качество воспроизведения звука увеличилось до момента, когда необходимо уменьшить качество воспроизведения видео.

`Notify` Задает для элемента данных **m \_ трсроттле** значение задержки, которое должно быть вставлено между кадрами [**сроттлеваит**](cbasevideorenderer-throttlewait.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




