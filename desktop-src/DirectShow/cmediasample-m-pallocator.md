---
description: Указатель на распределитель, создавший этот образец.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Элемент Кмедиасампле:: m_pAllocator (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665203"
---
# <a name="cmediasamplem_pallocator-member"></a>Элемент Кмедиасампле:: m \_ паллокатор

Указатель на распределитель, создавший этот образец.

## <a name="syntax"></a>Синтаксис


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Примечания

Несмотря на то, что образец хранит указатель на распределитель, он не содержит счетчик ссылок. Вместо этого распределитель увеличивает свой счетчик ссылок в методе [**имемаллокатор::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) IsReference и освобождает себя в методе [**Имемаллокатор:: релеасебуффер**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) . Это гарантирует, что распределитель будет доступен, пока другой объект использует этот пример.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




