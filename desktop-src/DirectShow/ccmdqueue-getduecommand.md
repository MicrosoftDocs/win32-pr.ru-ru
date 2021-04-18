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
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656892"
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

## <a name="remarks"></a>Комментарии

Эта функция-член блокируется до тех пор, пока не будет вызвана Ожидающая команда. Функция члена блокирует количество времени в миллисекундах, указанное в параметре *мстимеаут* . Команды времени потока становятся только между функциями-членами [**ккмдкуеуе:: Run**](ccmdqueue-run.md) и [**Ккмдкуеуе:: ендрун**](ccmdqueue-endrun.md) . Команда остается в очереди до выполнения или отмены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




