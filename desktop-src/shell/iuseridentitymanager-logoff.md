---
description: Выход из системы не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'Метод Иусеридентитиманажер:: logoff (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984156"
---
# <a name="iuseridentitymanagerlogoff-method"></a>Метод Иусеридентитиманажер:: logoff

\[**Выход из системы** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Не рекомендуется. Выйдите из текущего удостоверения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* \[ окне\]
</dt> <dd>

Тип: **HWND**

Значение **HWND** , определяющее окно, которое будет перенесено на передний план после завершения выхода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

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

[**иусеридентитиманажер**](iuseridentitymanager.md)
</dt> <dt>

[**Иусеридентитиманажер:: logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**Иусеридентитиманажер:: Манажеидентитиес**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




