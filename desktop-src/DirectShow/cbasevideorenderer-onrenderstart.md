---
description: Метод Онрендерстарт задает сведения для подготовки к просмотру.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Кбасевидеорендерер. Онрендерстарт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675011"
---
# <a name="cbasevideorendereronrenderstart-method"></a>Кбасевидеорендерер. Онрендерстарт, метод

`OnRenderStart`Метод задает сведения для подготовки к просмотру.

## <a name="syntax"></a>Синтаксис


```C++
void OnRenderStart(
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

## <a name="remarks"></a>Комментарии

Эта функция-член получает текущее время часов из системы и сохраняет ее в переменной-члене, используемой при завершении рисования. Функция также выполняет ведение журнала производительности. Эту функцию члена следует вызывать непосредственно перед началом рисования.

Эта функция члена переопределяет [**кбасерендерер:: онрендерстарт**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




