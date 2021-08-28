---
title: Метод IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Указывает, можно ли синхронизировать удаленный буфер обмена с локальным сеансом.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кансинкремотеклипбоардтолокалсессион
- Службы удаленных рабочих столов метода Кансинкремотеклипбоардтолокалсессион, интерфейс Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, метод Кансинкремотеклипбоардтолокалсессион
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 40a9fc5d6dcdc2e96d9ce916bce0567cccc90adf10fcacc5d797f61ed292c116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000844"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Метод Имсрдпклипбоард:: Кансинкремотеклипбоардтолокалсессион

Указывает, можно ли синхронизировать удаленный буфер обмена с локальным сеансом.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Параметры

**Значение true** , если удаленный буфер обмена можно синхронизировать с локальным сеансом; в противном случае — **значение false**.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>