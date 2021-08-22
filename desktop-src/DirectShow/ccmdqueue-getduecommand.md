---
description: Метод Жетдуекомманд извлекает указатель на следующую команду из-за.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Ккмдкуеуе. Жетдуекомманд, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6e7c8d133537dc2b185c755e65f3a4febbee762c5c2306de37ad0c627434df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016432"
---
# <a name="ccmdqueuegetduecommand-method"></a>Ккмдкуеуе. Жетдуекомманд, метод

`GetDueCommand`Метод получает указатель на следующую команду, которая вызвана.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ppCmd* 
</dt> <dd>

Адрес указателя на отложенную команду.

</dd> <dt>

*мстимеаут* 
</dt> <dd>

Время ожидания перед истечением времени ожидания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение "E \_ Abort", если истекло время ожидания. Возвращает значение \_ ОК, если выполнено успешно; в противном случае возвращает ошибку. Возвращает объект, который был увеличен с помощью **IUnknown:: AddRef**.

## <a name="remarks"></a>Remarks

Эта функция-член блокируется до тех пор, пока не будет вызвана Ожидающая команда. Функция члена блокирует количество времени в миллисекундах, указанное в параметре *мстимеаут* . Команды времени потока становятся только между функциями-членами [**ккмдкуеуе:: Run**](ccmdqueue-run.md) и [**Ккмдкуеуе:: ендрун**](ccmdqueue-endrun.md) . Команда остается в очереди до выполнения или отмены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




