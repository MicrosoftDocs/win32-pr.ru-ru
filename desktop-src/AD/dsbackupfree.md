---
title: Функция Дсбаккупфри (Нтдсбкли. h)
description: Освобождает память, выделенную функциями резервного копирования и восстановления домен Active Directory Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупфри
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891801"
---
# <a name="dsbackupfree-function"></a>Функция Дсбаккупфри

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Функция **дсбаккупфри** освобождает память, выделенную функциями резервного копирования и восстановления домен Active Directory Services. Следующие функции выделяют память, которая должна быть освобождена с помощью функции **дсбаккупфри** .

-   [**дсбаккупжетбаккуплогс**](dsbackupgetbackuplogs.md)
-   [**дсбаккупжетдатабасенамес**](dsbackupgetdatabasenames.md)
-   [**дсбаккуппрепаре**](dsbackupprepare.md)
-   [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a>Синтаксис


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвбуффер* \[ окне\]
</dt> <dd>

Указатель на буфер памяти, который необходимо освободить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

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

[**дсбаккупжетбаккуплогс**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**дсбаккупжетдатабасенамес**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**дсбаккуппрепаре**](dsbackupprepare.md)
</dt> <dt>

[**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[Резервное копирование сервера Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Функции резервного копирования каталога](directory-backup-functions.md)
</dt> </dl>

 

