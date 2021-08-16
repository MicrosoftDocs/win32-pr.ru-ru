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
ms.openlocfilehash: 479a1641a6d347837733da7e7d26e67b2011654e638681ec774a6ec5d931e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430254"
---
# <a name="dsbackupend-function"></a>Функция Дсбаккупенд

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. начиная с Windows Vista используйте вместо этого [служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

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

## <a name="remarks"></a>Remarks

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

 

