---
description: Метод NotReady сигнализирует, что переход состояния еще не завершен.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Кбасерендерер. NotReady, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669415"
---
# <a name="cbaserenderernotready-method"></a>Кбасерендерер. NotReady, метод

`NotReady`Метод сигнализирует, что переход состояния еще не завершен.

## <a name="syntax"></a>Синтаксис


```C++
void NotReady();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод приводит к тому, что метод [**кбасерендерер::**](cbaserenderer-getstate.md) noreturn возвращает в качестве \_ \_ промежуточного состояния VFW S \_ , что означает, что фильтр все еще переходит в текущее состояние. Фильтр вызывает этот метод при ожидании перехода состояния. (Это происходит, когда фильтр приостанавливается, пока не будет получен пример.)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> <dt>

[**чеккреади**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




