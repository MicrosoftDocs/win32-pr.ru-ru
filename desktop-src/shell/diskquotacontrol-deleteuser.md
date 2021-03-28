---
description: Удаляет пользователя из тома.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Дисккуотаконтрол. Делетеусер, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262905"
---
# <a name="diskquotacontroldeleteuser-method"></a>Дисккуотаконтрол. Делетеусер, метод

Удаляет пользователя из тома.

## <a name="syntax"></a>Синтаксис


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*аусер* 
</dt> <dd>

Тип: **объект**

Выражение объекта, результатом которого является объект [**дидисккуотаусер**](didiskquotauser-object.md) пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

Этот метод завершается сбоем, если пользователь владеет любым хранилищем на томе. Перед удалением пользователя из тома необходимо удалить все хранилища для этого пользователя, переместить его на другой том или передать его владение другому пользователю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Дсккуота. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**AddUser**](diskquotacontrol-adduser.md)
</dt> <dt>

[**дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




