---
description: Метод Ондиректрендер собирает сведения о времени, которые управляют синхронизацией и контролем качества.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Кбасевидеорендерер. Ондиректрендер, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675240"
---
# <a name="cbasevideorendererondirectrender-method"></a>Кбасевидеорендерер. Ондиректрендер, метод

Метод **ондиректрендер** собирает сведения о времени, которые управляют синхронизацией и контролем качества.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) примера мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Вызовите этот метод вместо [**онрендерстарт**](cbasevideorenderer-onrenderstart.md) и [**онрендеренд**](cbasevideorenderer-onrenderend.md). Этот метод используется модулем подготовки видео DirectDraw.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




