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
ms.openlocfilehash: 8fb16ae67ad5dcd9324c176a39a0dc9e566638ed960443496a0d556990bd8717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464404"
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

## <a name="requirements"></a>Requirements (Требования)



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

 

 




