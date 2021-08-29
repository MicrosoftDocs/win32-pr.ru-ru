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
ms.openlocfilehash: 6011bf839e2f91b3eb835cfe295e0c1845a6c6697a262c0f9bf7525d6c157565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884064"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/>    | Windows 2000 Server<br/>                                                         |
| Заголовок<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсидент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иусеридентитиманажер**](iuseridentitymanager.md)
</dt> <dt>

[**Иусеридентитиманажер:: logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**Иусеридентитиманажер:: Манажеидентитиес**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




