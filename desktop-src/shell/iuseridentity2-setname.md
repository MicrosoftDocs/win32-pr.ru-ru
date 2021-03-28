---
description: 'IUserIdentity2:: SetName не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'Метод IUserIdentity2:: SetName (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985680"
---
# <a name="iuseridentity2setname-method"></a>Метод IUserIdentity2:: SetName

\[**IUserIdentity2:: SetName** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Задает отображаемое имя удостоверения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pszName* \[ окне\]
</dt> <dd>

Тип: **WCHAR \** _

Строка расширенных символов, содержащая новое имя удостоверения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetName**](iuseridentity-getname.md)
</dt> </dl>

 

 




