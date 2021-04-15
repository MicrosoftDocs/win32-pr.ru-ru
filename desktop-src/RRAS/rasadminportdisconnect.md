---
title: Функция Расадминпортдисконнект (Рассапи. h)
description: Функция Расадминпортдисконнект отключает порт, который используется в данный момент.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RAS функции Расадминпортдисконнект
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676017"
---
# <a name="rasadminportdisconnect-function"></a>Функция Расадминпортдисконнект

\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0. Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003. Приложения должны использовать функцию [**мпрадминпортдисконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]

Функция **расадминпортдисконнект** отключает порт, который используется в данный момент.

## <a name="syntax"></a>Синтаксис


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзсервер* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя сервера удаленного доступа Windows NT или Windows 2000. Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.

</dd> <dt>

*лпсзпорт* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя порта на сервере.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов ошибок.



| Значение                                                                                               | Значение                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**Ошибка \_ недопустимого \_ порта**</dt> </dl> | Указан недопустимый порт.<br/>    |
| <dl> <dt>**НЕРР \_ усернотфаунд**</dt> </dl>   | Порт сейчас не используется.<br/> |



 

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
</dt> </dl>

 

