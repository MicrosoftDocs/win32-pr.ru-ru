---
description: Возвращает метод, который вызывается после завершения асинхронного действия.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Метод IAsyncAction:: get_Completed'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 90e26947f0771490334ee731b25576759943c44cc47a9fda6681da9aa1f11fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323445"
---
# <a name="iasyncactionget_completed-method"></a>Метод IAsyncAction:: Get \_ завершен

Возвращает метод, который вызывается после завершения асинхронного действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обработчик событий* \[ заполняет\]
</dt> <dd>

Тип: **[ **асинкактионкомплетедхандлер**](asyncactioncompletedhandler.md)\*\***

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

 

 
