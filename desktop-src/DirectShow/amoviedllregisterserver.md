---
description: Является устаревшей. Вместо этого используйте AMovieDllRegisterServer2.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Функция Амовиедллрегистерсервер (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689050"
---
# <a name="amoviedllregisterserver-function"></a>Функция Амовиедллрегистерсервер

Является устаревшей. Вместо этого используйте [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AMovieDllRegisterServer(void);
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

 

 




