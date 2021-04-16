---
description: Метод Render визуализирует образец.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Метод Кбасерендерер. Render (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658046"
---
# <a name="cbaserendererrender-method"></a>Кбасерендерер. Render, метод

`Render`Метод подготавливает к просмотру пример.

## <a name="syntax"></a>Синтаксис


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующей таблице.



| Код возврата                                                                             | Описание                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Фильтр остановлен или *пмедиасампле* имеет **значение NULL**.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                                              |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывает чистый виртуальный метод [**кбасерендерер::D орендерсампле**](cbaserenderer-dorendersample.md), который выполняет реальную работу. Производный класс должен реализовывать **дорендерсампле**.

Непосредственно перед вызовом **дорендерсампле** этот метод вызывает метод [**Кбасерендерер:: онрендерстарт**](cbaserenderer-onrenderstart.md) . Сразу же после этого вызывается метод [**кбасерендерер:: онрендеренд**](cbaserenderer-onrenderend.md) . Производный класс может переопределить эти два метода по мере необходимости.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




