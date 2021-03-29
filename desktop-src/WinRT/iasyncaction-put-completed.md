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
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991124"
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

Тип: **[**асинкактионкомплетедхандлер**](asyncactioncompletedhandler.md) \** _

Метод, обрабатывающий уведомление о завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

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

 

 
