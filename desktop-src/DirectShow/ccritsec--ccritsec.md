---
description: Метод деструктора Ккритсек. ~ Ккритсек.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Деструктор Ккритсек. ~ Ккритсек (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095812"
---
# <a name="ccritsecccritsec-destructor"></a>Деструктор Ккритсек. ~ Ккритсек

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CCritSec();
```



## <a name="remarks"></a>Remarks

Этот метод вызывает функцию [**делетекритикалсектион**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) для удаления критической секции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

