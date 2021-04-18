---
description: Уведомляет систему, что приложение сохранило свои данные и готово к приостановке.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'Метод Исуспендингдеферрал:: Complete (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711057"
---
# <a name="isuspendingdeferralcomplete-method"></a>Метод Исуспендингдеферрал:: Complete

Уведомляет систему, что приложение сохранило свои данные и готово к приостановке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

[**исуспендингдеферрал**](isuspendingdeferral.md)
</dt> </dl>

 

 




