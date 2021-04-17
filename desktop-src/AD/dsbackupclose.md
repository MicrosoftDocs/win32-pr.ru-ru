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
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490251"
---
# <a name="dsbackupclose-function"></a>Функция Дсбаккупклосе

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

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

[**дсбаккупопенфиле**](dsbackupopenfile.md)
</dt> <dt>

[**дсбаккуппрепаре**](dsbackupprepare.md)
</dt> <dt>

[Резервное копирование сервера Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Функции резервного копирования каталога](directory-backup-functions.md)
</dt> </dl>

 

