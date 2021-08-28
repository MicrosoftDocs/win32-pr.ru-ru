---
description: Метод Run переключается в режим выполнения, чтобы можно было выполнить команды, отложенные в потокового времени.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Метод Ккмдкуеуе. Run (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5da70c4ac0c5890e4483f7facdc4d1f5a3d5dd70906c53917bd83029dfaa6c6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757144"
---
# <a name="ccmdqueuerun-method"></a>Ккмдкуеуе. Run, метод

`Run`Метод переключается в режим выполнения, чтобы можно было выполнить команды, отложенные потоком времени.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тстреамтимеоффсет* 
</dt> <dd>

Время смещения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Во время выполнения поддерживается сопоставление потоков во время презентации.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




