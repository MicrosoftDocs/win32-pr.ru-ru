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
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695509"
---
# <a name="dssetauthidentity-function"></a>Функция Дссетаусидентити

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. начиная с Windows Vista используйте вместо этого [служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

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

## <a name="remarks"></a>Remarks

Если **дссетаусидентити** не вызывается, предполагается, что используется контекст безопасности текущего процесса.

## <a name="requirements"></a>Requirements (Требования)



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

 

