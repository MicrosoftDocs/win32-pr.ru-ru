---
description: Метод DataReader возвращает указатель на интерфейс Иасинкреадер выходного контакта.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Метод Кпуллпин. DataReader (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7880cba8e910c3da8ade049e18ae22e403c0c616246e4dfde94e587a1fcdeab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055004"
---
# <a name="cpullpingetreader-method"></a>Кпуллпин. DataReader, метод

`GetReader`Метод возвращает указатель на интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) выходного контакта.

## <a name="syntax"></a>Синтаксис


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

## <a name="remarks"></a>Remarks

Возвращенный интерфейс имеет необработанный счетчик ссылок. Вызывающий объект должен освободить интерфейс.

метод не проверяет значение указателя интерфейса перед вызовом **AddRef**, поэтому не вызывайте его до тех пор, пока не будет успешно вызван метод [**кпуллпин:: Подключение**](cpullpin-connect.md) . В противном случае указатель интерфейса может иметь **значение NULL** , а вызов **AddRef** выдаст исключение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




