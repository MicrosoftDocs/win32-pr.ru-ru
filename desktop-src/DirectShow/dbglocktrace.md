---
description: Включает или отключает ведение журнала отладки для данного критического раздела.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Функция Дбглокктраце (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b55736b2efb8fd4cfbca40710caa930c200c84e1ceec9c8c4f7439468c1add1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654074"
---
# <a name="dbglocktrace-function"></a>Функция Дбглокктраце

Включает или отключает ведение журнала отладки для данного критического раздела.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пккрит* 
</dt> <dd>

Указатель на критический раздел [**ккритсек**](ccritsec.md) .

</dd> <dt>

*фтраце* 
</dt> <dd>

Значение, указывающее, включено ли ведение журнала. Используйте **значение true** , чтобы включить ведение журнала, или **false** , чтобы отключить его.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция используется для трассировки определенной критической секции. По умолчанию ведение журнала отладки критических разделов отключено из-за большого количества критических разделов.

Чтобы выполнить трассировку критической секции, выполните следующие действия.

1.  определите отладку или \_ отладку перед включением заголовков DirectShow.
2.  Включите ведение журнала отладки для критически важных разделов, вызвав [**дбгсетмодулелевел**](dbgsetmodulelevel.md) с \_ флагом блокировки журнала.
3.  Вызовите **дбглокктраце** в критическом разделе, который необходимо отследить.

В розничных сборках функция **дбглокктраце** не действует.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как отслеживать критическую секцию.


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции отладки критического раздела](critical-section-debugging-functions.md)
</dt> </dl>

 

 




