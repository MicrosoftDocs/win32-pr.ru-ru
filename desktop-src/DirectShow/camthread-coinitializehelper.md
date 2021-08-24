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
ms.openlocfilehash: 41a763a4b9151f22615aa0af3dae57af8281751209a016dc3135f3572e9d8ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768294"
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



 

## <a name="remarks"></a>Remarks

Метод [**камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) вызывает этот вспомогательный метод, который вызывает функцию CoInitializeEx. \_ \_ для отключения платформа динамических данных Exchange (DDE) используется флаг деинициализации disable OLE1DDE. Дополнительные сведения см. в разделе пакет SDK для платформы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




