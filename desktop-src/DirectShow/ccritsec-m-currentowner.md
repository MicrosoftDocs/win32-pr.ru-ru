---
description: Идентификатор потока владеющего потока.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Элемент Ккритсек:: m_currentOwner (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657953"
---
# <a name="ccritsecm_currentowner-member"></a>Элемент Ккритсек:: m \_ куррентовнер

Идентификатор потока владеющего потока.

## <a name="syntax"></a>Синтаксис


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Примечания

Эта переменная-член определена только в отладочной версии базового класса. [Функции отладки критического раздела](critical-section-debugging-functions.md) используют этот элемент.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

 




