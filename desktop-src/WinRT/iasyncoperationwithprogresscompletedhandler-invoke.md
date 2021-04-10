---
description: Вызывает метод, который вызывается, когда заданная асинхронная операция сообщает о ходе выполнения.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>:: Invoke метод'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145130"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>:: Invoke метод

Вызывает метод, который вызывается, когда заданная асинхронная операция сообщает о ходе выполнения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*асинЦинфо* \[ окне\]
</dt> <dd>

Введите: **[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _

Асинхронное действие, которое сообщает о завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>           |
| Минимальная версия сервера<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
