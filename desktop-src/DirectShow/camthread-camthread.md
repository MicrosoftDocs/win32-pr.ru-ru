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
ms.openlocfilehash: e042624573cd0c421e8ecd202cde971a49eef95cc5f3c6c0ac64bf45b4cf9c19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103334"
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
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




