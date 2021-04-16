---
description: Флаг, указывающий, отправляет ли окно сообщение об уничтожении.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Элемент Кбасевиндов:: m_bDoPostToDestroy (Винутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657694"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Элемент Кбасевиндов:: m \_ бдопосттодестрой

Флаг, указывающий, отправляет ли окно сообщение об уничтожении. Если **значение — true**, метод [**Кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) использует функцию посылки **сообщений** для отправки частного сообщения об уничтожении. Если **значение равно false**, **Доневисвиндов** использует функцию **SendMessage** для отправки сообщения. По умолчанию используется значение **false**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




