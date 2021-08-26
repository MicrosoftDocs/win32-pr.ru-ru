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
ms.openlocfilehash: 1f6f83f7310700e774692d876bda979343da80aa45ea8012bf187e50f0af67bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028454"
---
# <a name="rasadminservergetinfo-function"></a>Функция Расадминсервержетинфо

\[эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0. он возвращает \_ вызов ошибки \_ \_ , не реализованный на сервере Windows 2003. Приложения должны использовать функцию [**мпрадминсервержетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]

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

указатель на строку в юникоде, заканчивающуюся **нулем,** которая указывает имя сервера RAS Windows NT/Windows 2000. Если этот параметр имеет **значение NULL**, функция возвращает сведения о локальном компьютере. Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.

</dd> <dt>

*pRasServer0* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**RAS \_ Server \_ 0**](ras-server-0-str.md) , которая получает количество портов, настроенных на сервере, количество используемых в данный момент портов и номер версии сервера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение является кодом ошибки. Возможные коды ошибок включают данные, возвращаемые [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для функции [**каллнамедпипе**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) . Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте **GetLastError**.

## <a name="remarks"></a>Remarks

Чтобы перечислить все серверы RAS в домене, вызовите функцию [**нетсерверенум**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) и укажите \_ тип ООКП \_ для параметра *serverType* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/> | Windows 2000 Server<br/>                                                         |
| Заголовок<br/>                | <dl> <dt>Рассапи. h</dt> </dl>   |
| Библиотека<br/>               | <dl> <dt>Рассапи. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Функции администрирования сервера RAS](ras-server-administration-functions.md)
</dt> <dt>

[**нетсерверенум**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**\_Сервер RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

