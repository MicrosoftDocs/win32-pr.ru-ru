---
description: 'Метод Сетпреролл указывает, является ли этот пример примером предобразца. Образец не должен отображаться. Этот метод реализует метод Имедиасампле:: Сетпреролл.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Кмедиасампле. Сетпреролл, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674978"
---
# <a name="cmediasamplesetpreroll-method"></a>Кмедиасампле. Сетпреролл, метод

`SetPreroll`Метод указывает, является ли этот пример примером предобразца. Образец не должен отображаться. Этот метод реализует метод [**имедиасампле:: сетпреролл**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*биспреролл* 
</dt> <dd>

Логическое значение, указывающее, является ли этот пример примером. Если **значение равно true**, это пример предобразца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод обновляет переменную члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает свойство "предвращение".

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




