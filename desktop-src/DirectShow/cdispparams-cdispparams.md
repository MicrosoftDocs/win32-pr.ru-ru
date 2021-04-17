---
description: Метод конструктора.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Конструктор Кдисппарамс. Кдисппарамс (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675812"
---
# <a name="cdispparamscdispparams-constructor"></a>Кдисппарамс. Кдисппарамс, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*наргс* 
</dt> <dd>

Количество аргументов, переданных методу или свойству.

</dd> <dt>

*паргс* 
</dt> <dd>

Указатель на список аргументов. В списке каждый аргумент сохраняется с типом Variant.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдисппарамс**](cdispparams.md)
</dt> </dl>

 

 




