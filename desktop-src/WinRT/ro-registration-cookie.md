---
description: Представляет фабрики активации, зарегистрированные путем вызова функции Рорегистерактиватионфакториес.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Роапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741601"
---
# <a name="ro_registration_cookie"></a>\_ \_ файл cookie регистрации ro

Представляет фабрики активации, зарегистрированные путем вызова функции [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Remarks

функция [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) возвращает **\_ \_ файл COOKIE регистрации RO** , если фабрики класса активируемого зарегистрированы в среда выполнения Windows. Функция [**роревокеактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) использует файл cookie для удаления фабрик класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Роапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**роревокеактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
