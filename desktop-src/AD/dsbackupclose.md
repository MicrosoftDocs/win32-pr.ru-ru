---
title: Функция Дсбаккупклосе (Нтдсбкли. h)
description: Закрывает файл резервной копии, Открытый с помощью функции Дсбаккупопенфиле.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупклосе
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c9c8931d67b33fdad1f9e3605ee6efe801dac988d3931d96d1417561c093b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192192"
---
# <a name="dsbackupclose-function"></a>Функция Дсбаккупклосе

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. начиная с Windows Vista используйте вместо этого [служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Функция **дсбаккупклосе** закрывает файл резервной копии, Открытый с помощью функции [**дсбаккупопенфиле**](dsbackupopenfile.md) . Для каждого маркера резервного копирования в каждый момент времени может быть открыт только один файл, поэтому эта функция закрывает открытый в данный момент файл.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DsBackupClose(
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

</dd> <dt>

**хринвалидхандле**
</dt> <dd>

В настоящее время файл не открыт.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Нтдсбкли. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нтдсбкли. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дсбаккупопенфиле**](dsbackupopenfile.md)
</dt> <dt>

[**дсбаккуппрепаре**](dsbackupprepare.md)
</dt> <dt>

[Резервное копирование сервера Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Функции резервного копирования каталога](directory-backup-functions.md)
</dt> </dl>

 

