---
description: IUserIdentity2 не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Интерфейс IUserIdentity2 (Мсидент. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539485"
---
# <a name="iuseridentity2-interface"></a>Интерфейс IUserIdentity2

\[**IUserIdentity2** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Предоставляет методы, предоставляющие имена, пароли и порядковые номера для конкретного удостоверения пользователя.

## <a name="members"></a>Элементы

Интерфейс **IUserIdentity2** наследует от [**иусеридентити**](iuseridentity.md). **IUserIdentity2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IUserIdentity2** содержит следующие методы.



| Метод                                                  | Описание                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword;**](iuseridentity2-changepassword.md) | Не рекомендуется. Задает новый пароль для удостоверения.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Не рекомендуется. Возвращает порядковый номер этого удостоверения.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Не рекомендуется. Задает отображаемое имя удостоверения.<br/>     |



 

## <a name="remarks"></a>Примечания

Этот интерфейс также предоставляет методы интерфейса [**иусеридентити**](iuseridentity.md) , от которых он наследуется.

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

[**IUserIdentity**](iuseridentity.md)
</dt> </dl>

 

 




