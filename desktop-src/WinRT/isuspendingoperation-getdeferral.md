---
description: Запрашивает задержку операции приостановки выполнения приложения.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Метод Исуспендингоператион:: откладывания (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897378"
---
# <a name="isuspendingoperationgetdeferral-method"></a>Метод Исуспендингоператион:: откладывания

Запрашивает задержку операции приостановки выполнения приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*РБП* \[ out, retval\]
</dt> <dd>

Приостановка отсрочки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исуспендингоператион**](isuspendingoperation.md)
</dt> </dl>

 

 




