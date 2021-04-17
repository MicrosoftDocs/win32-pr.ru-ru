---
description: Пример очереди носителя.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Элемент Каутпуткуеуе:: m_List (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675534"
---
# <a name="coutputqueuem_list-member"></a>Элемент списка Каутпуткуеуе:: m \_

Пример очереди носителя.

## <a name="syntax"></a>Синтаксис


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Примечания

Эта переменная-член является указателем на объект [**кженериклист**](cgenericlist.md) , содержащий указатели [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Тип **ксамплелист** определяется следующим образом:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




