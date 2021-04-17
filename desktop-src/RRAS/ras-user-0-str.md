---
title: Структура RAS_USER_0 (Рассапи. h)
description: '\_Структура пользователя RAS \_ 0 используется в функциях Расадминусерсетинфо и расадминусержетинфо для указания сведений о пользователе.'
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS структуры RAS_USER_0
- RAS — указатель структуры PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534103"
---
# <a name="ras_user_0-structure"></a>\_Структура пользователя RAS \_ 0

\[Эта версия структуры **пользователя RAS \_ \_ 0** не поддерживается в Windows Vista. Используйте более новый [**\_ пользователь RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) , определенный в мпрапи. h.\]

Структура **\_ пользователя RAS \_ 0** используется в функциях [**расадминусерсетинфо**](rasadminusersetinfo.md) и [**расадминусержетинфо**](rasadminusergetinfo.md) для указания сведений о пользователе.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Члены

<dl> <dt>

**бфпривилеже**
</dt> <dd>

Набор битовых флагов, задающих права доступа RAS для пользователя. Этот член может быть сочетанием \_ флага расприв диалинпривилеже и одним из флагов обратного вызова. Используйте \_ маску КАЛЛБАККТИПЕ расприв, чтобы указать тип привилегий обратного вызова, предоставленный пользователю. Определены следующие флаги.



| Значение                                                                                                                                                                                                                                         | Значение                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**\_Обратный вызов расприв**</dt> </dl>                             | У пользователя нет прав на обратный вызов.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**РАСПРИВ \_ админсеткаллбакк**</dt> </dl>     | Учетная запись пользователя настроена так, чтобы администратор установил номер обратного вызова.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**РАСПРИВ \_ каллерсеткаллбакк**</dt> </dl> | Удаленный пользователь может указать номер телефона для обратного вызова при наборе номера.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**РАСПРИВ \_ диалинпривилеже**</dt> </dl>         | Пользователь имеет разрешение на вызов на этом сервере.<br/>                                 |



 

Укажите один из флагов обратного вызова в вызове функции [**расадминусерсетинфо**](rasadminusersetinfo.md) .

</dd> <dt>

**сзфоненумбер**
</dt> <dd>

Строка в Юникоде, заканчивающаяся нулем, которая указывает номер телефона для обратного вызова для пользователя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Рассапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Структуры администрирования сервера RAS](ras-server-administration-structures.md)
</dt> <dt>

[**расадминусержетинфо**](rasadminusergetinfo.md)
</dt> <dt>

[**расадминусерсетинфо**](rasadminusersetinfo.md)
</dt> </dl>

 

 





