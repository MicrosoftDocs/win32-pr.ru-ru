---
description: 'Метод Receive получает следующий образец носителя в потоке. Этот метод переопределяет метод Кбасеинпутпин:: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Метод Крендереринпутпин. Receive (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658007"
---
# <a name="crendererinputpinreceive-method"></a>Крендереринпутпин. Receive, метод

`Receive`Метод получает следующий пример носителя в потоке. Этот метод переопределяет метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Receive(
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

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**кбасерендерер:: Receive**](cbaserenderer-receive.md) фильтра, который обрабатывает отрисовку. В случае сбоя этого метода ПИН-код отправляет \_ событие EC еррораборт.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Крендереринпутпин**](crendererinputpin.md)
</dt> </dl>

 

 




