---
title: Функция Расадминсервержетинфо (Рассапи. h)
description: Функция Расадминсервержетинфо возвращает конфигурацию сервера RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RAS функции Расадминсервержетинфо
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676015"
---
# <a name="rasadminservergetinfo-function"></a>Функция Расадминсервержетинфо

\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0. Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003. Приложения должны использовать функцию [**мпрадминсервержетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]

Функция **расадминсервержетинфо** возвращает конфигурацию сервера RAS.

## <a name="syntax"></a>Синтаксис


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзсервер* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, заканчивающуюся **нулем,** которая указывает имя сервера удаленного доступа Windows NT или Windows 2000. Если этот параметр имеет **значение NULL**, функция возвращает сведения о локальном компьютере. Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.

</dd> <dt>

*pRasServer0* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**RAS \_ Server \_ 0**](ras-server-0-str.md) , которая получает количество портов, настроенных на сервере, количество используемых в данный момент портов и номер версии сервера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение является кодом ошибки. Возможные коды ошибок включают данные, возвращаемые [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для функции [**каллнамедпипе**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) . Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте **GetLastError**.

## <a name="remarks"></a>Комментарии

Чтобы перечислить все серверы RAS в домене, вызовите функцию [**нетсерверенум**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) и укажите \_ тип ООКП \_ для параметра *serverType* .

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

[**нетсерверенум**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**\_Сервер RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

