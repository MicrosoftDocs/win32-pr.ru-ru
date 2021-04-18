---
description: Представляет фабрики активации, зарегистрированные путем вызова функции Рорегистерактиватионфакториес.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Роапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701570"
---
# <a name="ro_registration_cookie"></a>\_ \_ файл cookie регистрации ro

Представляет фабрики активации, зарегистрированные путем вызова функции [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Комментарии

Функция [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) возвращает **\_ \_ файл cookie регистрации ro** , если фабрики класса активируемого зарегистрированы в среда выполнения Windows. Функция [**роревокеактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) использует файл cookie для удаления фабрик класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                     |
| Header<br/>                   | <dl> <dt>Роапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**роревокеактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
