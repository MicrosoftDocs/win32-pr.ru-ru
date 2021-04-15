---
description: Является устаревшей. Вместо этого используйте AMovieDllRegisterServer2.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Функция Амовиедллунрегистерсервер (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689221"
---
# <a name="amoviedllunregisterserver-function"></a>Функция Амовиедллунрегистерсервер

Является устаревшей. Вместо этого используйте [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дллсетуп. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции установки DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




