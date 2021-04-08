---
title: Функция Дсбаккупенд (Нтдсбкли. h)
description: Вызывается для завершения операции резервного копирования.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупенд
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891802"
---
# <a name="dsbackupend-function"></a>Функция Дсбаккупенд

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Для завершения операции резервного копирования вызывается функция **дсбаккупенд** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ХБК* \[ окне\]
</dt> <dd>

Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае. В следующем списке перечислены другие возможные коды ошибок.

<dl> <dt>

**Ошибка \_ недопустимого \_ параметра**
</dt> <dd>

Недопустимый *ХБК* .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Функция **дсбаккупенд** закрывает необработанные дескрипторы привязки и выполняет очистку после успешной или неудачной попытки резервного копирования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Нтдсбкли. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нтдсбкли. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дссетаусидентити**](dssetauthidentity.md)
</dt> <dt>

[Резервное копирование сервера Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Функции резервного копирования каталога](directory-backup-functions.md)
</dt> </dl>

 

