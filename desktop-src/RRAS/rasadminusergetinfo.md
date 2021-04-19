---
title: Функция Расадминусержетинфо (Рассапи. h)
description: Функция Расадминусержетинфо получает разрешения RAS и сведения о номере телефона обратного вызова для указанного пользователя.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RAS функции Расадминусержетинфо
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675457"
---
# <a name="rasadminusergetinfo-function"></a>Функция Расадминусержетинфо

\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0. Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003. Приложения должны использовать функцию [**мпрадминусержетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]

Функция **расадминусержетинфо** получает разрешения RAS и сведения о номере телефона обратного вызова для указанного пользователя.

## <a name="syntax"></a>Синтаксис


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзусераккаунтсервер* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя основного или резервного контроллера домена с базой данных учетных записей пользователей. Используйте функцию [**расадминжетусераккаунтсервер**](rasadmingetuseraccountserver.md) для получения имени этого сервера.

</dd> <dt>

*лпсзусер* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя пользователя, для которого необходимо получить сведения об RAS.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Указатель на структуру [**\_ пользователя RAS \_ 0**](ras-user-0-str.md) , которая получает данные RAS для указанного пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.



| Значение                                                                                            | Значение                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**НЕРР \_ буфтусмалл**</dt> </dl> | Недостаточно памяти для выполнения этой функции.<br/> |



 

Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Рассапи. h</dt> </dl>   |
| Библиотека<br/>               | <dl> <dt>Рассапи. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Функции администрирования сервера RAS](ras-server-administration-functions.md)
</dt> <dt>

[**\_Пользователь RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**расадминжетусераккаунтсервер**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**расадминусерсетинфо**](rasadminusersetinfo.md)
</dt> </dl>

 

