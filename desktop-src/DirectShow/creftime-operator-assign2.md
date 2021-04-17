---
description: Оператор = назначает новое время ссылки. Этот метод использует параметр *LL* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Крефтиме. operator = метод (Рефтиме. h) — параметр LL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187841"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>Крефтиме. operator = метод (Рефтиме. h) — параметр LL

Оператор = назначает новое время ссылки.

## <a name="syntax"></a>Синтаксис


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*залив* 
</dt> <dd>

Новое время ссылки в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок  | Рефтиме. h (включение Streams. h)                                                                                   |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |



 

 




