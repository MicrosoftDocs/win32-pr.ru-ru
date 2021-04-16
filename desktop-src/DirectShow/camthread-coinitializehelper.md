---
description: Метод Коинитиализехелпер вызывает функцию CoInitializeEx в начале потока.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Камсреад. Коинитиализехелпер, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657159"
---
# <a name="camthreadcoinitializehelper-method"></a>Камсреад. Коинитиализехелпер, метод

`CoInitializeHelper`Метод вызывает функцию CoInitializeEx в начале потока.

## <a name="syntax"></a>Синтаксис


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                             | Описание                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Функция CoInitializeEx недоступна.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                                      |
| <dl> <dt>**\_Ошибка E**</dt> </dl>  | Ошибка.<br/>                                      |



 

## <a name="remarks"></a>Комментарии

Метод [**камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) вызывает этот вспомогательный метод, который вызывает функцию CoInitializeEx. \_ \_ Для отключения платформа динамических данных Exchange (DDE) используется флаг деinit Disable OLE1DDE. Дополнительные сведения см. в разделе пакет SDK для платформы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




