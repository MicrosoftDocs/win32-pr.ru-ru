---
description: Запрашивает задержку операции приостановки выполнения приложения.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: Метод Исуспендингоператион::-отсрочки (Windows. ApplicationModel. h)
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
ms.openlocfilehash: 4a64ed4449c2e11ebeec9194adb7fd69ecc7227efa9df36a6900f4139e44ec4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794994"
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
| Заголовок<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исуспендингоператион**](isuspendingoperation.md)
</dt> </dl>

 

 




