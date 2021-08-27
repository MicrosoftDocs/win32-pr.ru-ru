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
ms.openlocfilehash: 3e261116961f23c845ec2e27c6f20748b2c50cd9c036d9bc7d42bfe24b9b4fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087074"
---
# <a name="coutputqueuem_list-member"></a>Элемент списка Каутпуткуеуе:: m \_

Пример очереди носителя.

## <a name="syntax"></a>Синтаксис


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Remarks

Эта переменная-член является указателем на объект [**кженериклист**](cgenericlist.md) , содержащий указатели [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Тип **ксамплелист** определяется следующим образом:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




