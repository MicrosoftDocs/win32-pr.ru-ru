---
description: Метод Онрендеренд выполняет сглаживание для случаев, когда время отрисовки меняется из-за прерываний.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Кбасевидеорендерер. Онрендеренд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d622ec62b27ae2e85eb9bef37516c82acbb17e03bef9a51b161edacd0b95c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658692"
---
# <a name="cbasevideorendereronrenderend-method"></a>Кбасевидеорендерер. Онрендеренд, метод

`OnRenderEnd`Метод выполняет сглаживание для случаев, когда время отрисовки меняется из-за прерываний.

## <a name="syntax"></a>Синтаксис


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на пример носителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Эту функцию члена следует вызывать сразу после рисования изображения.

Эта функция члена переопределяет [**кбасерендерер:: онрендеренд**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




