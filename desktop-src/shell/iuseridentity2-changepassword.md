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
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092701"
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

Тип: **WCHAR \***

Строка расширенных символов, содержащая пароль, который в настоящее время связан с удостоверением.

</dd> <dt>

*сзневпасс* \[ окне\]
</dt> <dd>

Тип: **WCHAR \***

Строка расширенных символов, содержащая новый пароль, который должен быть связан с удостоверением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

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



 

 




