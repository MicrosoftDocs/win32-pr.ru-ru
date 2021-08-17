---
description: Задает метод, который вызывается при завершении асинхронного действия.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: 'IAsyncAction: метод ut_Completed:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: aff219d5e6847c64034eed1b057e300ea601eedaa8aa7a131f1467aeacc42422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323167"
---
# <a name="iasyncactionput_completed-method"></a>IAsyncAction: метод:p UT \_ завершен

Задает метод, который вызывается при завершении асинхронного действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обработчик событий* \[ заполняет\]
</dt> <dd>

Тип: **[ **асинкактионкомплетедхандлер**](asyncactioncompletedhandler.md)\***

Метод, обрабатывающий уведомление о завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
