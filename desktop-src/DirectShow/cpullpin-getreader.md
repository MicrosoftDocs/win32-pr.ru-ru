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
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669055"
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

## <a name="remarks"></a>Комментарии

Возвращенный интерфейс имеет необработанный счетчик ссылок. Вызывающий объект должен освободить интерфейс.

Метод не проверяет значение указателя интерфейса перед вызовом **AddRef**, поэтому не вызывайте его до тех пор, пока не будет успешно вызван метод [**Кпуллпин:: Connect**](cpullpin-connect.md) . В противном случае указатель интерфейса может иметь **значение NULL** , а вызов **AddRef** выдаст исключение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




