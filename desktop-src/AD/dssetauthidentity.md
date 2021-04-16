---
title: Функция Дссетаусидентити (Нтдсбкли. h)
description: Задает контекст безопасности, в котором вызываются API-интерфейсы резервного копирования каталога.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дссетаусидентити
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491235"
---
# <a name="dssetauthidentity-function"></a>Функция Дссетаусидентити

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Функция **дссетаусидентити** задает контекст безопасности, в котором вызываются API-интерфейсы резервного копирования каталога.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сзусернаме* \[ окне\]
</dt> <dd>

Строка, завершающаяся нулем, которая указывает имя пользователя.

</dd> <dt>

*сздомаиннаме* \[ окне\]
</dt> <dd>

Строка, завершающаяся нулем, которая указывает имя домена, к которому принадлежит пользователь.

</dd> <dt>

*сзпассворд* \[ окне\]
</dt> <dd>

Строка, завершающаяся нулем, которая указывает пароль пользователя в указанном домене.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвращает стандартные коды успешного выполнения **HRESULT** . в противном случае возвращается код ошибки.

## <a name="remarks"></a>Комментарии

Если **дссетаусидентити** не вызывается, предполагается, что используется контекст безопасности текущего процесса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Нтдсбкли. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нтдсбкли. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Дссетаусидентитив** (Юникод) и **дссетаусидентитя** (ANSI)<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Резервное копирование и восстановление сервера Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Функции резервного копирования каталога](directory-backup-functions.md)
</dt> </dl>

 

