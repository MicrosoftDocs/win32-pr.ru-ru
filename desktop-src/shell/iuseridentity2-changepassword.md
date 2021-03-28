---
description: ChangePassword не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'Метод IUserIdentity2:: ChangePassword (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984605"
---
# <a name="iuseridentity2changepassword-method"></a>Метод IUserIdentity2:: ChangePassword

\[**ChangePassword** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Задает новый пароль для удостоверения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сзолдпасс* \[ окне\]
</dt> <dd>

Тип: **WCHAR \** _

Строка расширенных символов, содержащая пароль, который в настоящее время связан с удостоверением.

</dd> <dt>

_szNewPass * \[ в\]
</dt> <dd>

Тип: **WCHAR \** _

Строка расширенных символов, содержащая новый пароль, который должен быть связан с удостоверением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Примечания

Значение параметра *сзолдпасс* должно соответствовать текущему паролю удостоверения, применяемого для *сзневпасс* . Неправильное значение *сзолдпасс* приведет к возвращению значения E с \_ ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсидент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




