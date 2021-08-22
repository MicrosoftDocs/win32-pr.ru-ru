---
description: Метод Инитиалсреадпрок вызывает основную процедуру потока.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Iniметод Тиалсреадпрок (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540304"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Iniметод Тиалсреадпрок

`InitialThreadProc`Метод вызывает основную процедуру потока.

## <a name="syntax"></a>Синтаксис


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PV* 
</dt> <dd>

`this` вид.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , возвращаемое функцией [**Камсреад:: среадпрок**](camthread-threadproc.md). Это значение определяется производным классом.

## <a name="remarks"></a>Remarks

Метод [**камсреад:: Create**](camthread-create.md) использует этот метод для процедуры потока при создании потока. В нем используется `this` указатель в качестве аргумента потока.

Этот метод вызывает метод [**камсреад:: коинитиализехелпер**](camthread-coinitializehelper.md) , а затем среадпрок.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




