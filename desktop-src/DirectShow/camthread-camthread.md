---
description: Метод конструктора Камсреад. Камсреад.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Конструктор Камсреад. Камсреад (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096412"
---
# <a name="camthreadcamthread-constructor"></a>Камсреад. Камсреад, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** . Если конструктор завершается неудачно, этот параметр получает код ошибки. Если это происходит, объект находится в недопустимом состоянии.

Для обеспечения обратной совместимости с более ранними версиями стрмбасе. lib этот параметр по умолчанию **имеет значение NULL**. Однако рекомендуется передать значение, отличное от **null** , чтобы вызывающий объект мог проверить состояние объекта.

</dd> </dl>

## <a name="remarks"></a>Remarks

Метод конструктора не создает поток. Чтобы создать поток, вызовите метод [**камсреад:: Create**](camthread-create.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




