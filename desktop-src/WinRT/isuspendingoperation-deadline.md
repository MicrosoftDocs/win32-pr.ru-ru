---
description: Возвращает время, оставшееся до того, как будет продолжаться операция приостановки отложенного приложения.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: 'Исуспендингоператион: свойство еадлине:D (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 448f4d89ec2f1b7e3f68255897b32b3f4cba2ec753ae8f6cc7751c9041b01266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121504"
---
# <a name="isuspendingoperationdeadline-property"></a>Исуспендингоператион: свойство еадлине:D

Возвращает время, оставшееся до того, как будет продолжаться операция приостановки отложенного приложения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a>Значение свойства

Время, оставшееся до того, как будет приостановлена отложенная операция приостановки приложения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Заголовок<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**исуспендингоператион**](isuspendingoperation.md)
</dt> </dl>

 

 




