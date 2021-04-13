---
description: Метод конструктора.
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
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657871"
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

## <a name="remarks"></a>Комментарии

Метод конструктора не создает поток. Чтобы создать поток, вызовите метод [**камсреад:: Create**](camthread-create.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




