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
ms.openlocfilehash: 646c6fb7f8236aca87b5aebd1d30fd67750d960da4445d45bf45d8b601320274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156546"
---
# <a name="cmediasamplem_pallocator-member"></a>Элемент Кмедиасампле:: m \_ паллокатор

Указатель на распределитель, создавший этот образец.

## <a name="syntax"></a>Синтаксис


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Remarks

Несмотря на то, что образец хранит указатель на распределитель, он не содержит счетчик ссылок. Вместо этого распределитель увеличивает свой счетчик ссылок в методе [**имемаллокатор::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) IsReference и освобождает себя в методе [**Имемаллокатор:: релеасебуффер**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) . Это гарантирует, что распределитель будет доступен, пока другой объект использует этот пример.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




