---
title: Метод IMsRdpClipboard CanSyncLocalClipboardToRemoteSession
description: Указывает, можно ли синхронизировать локальный буфер обмена с удаленным сеансом.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кансинклокалклипбоардторемотесессион
- Службы удаленных рабочих столов метода Кансинклокалклипбоардторемотесессион, интерфейс Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, метод Кансинклокалклипбоардторемотесессион
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719218"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>Метод Имсрдпклипбоард:: Кансинклокалклипбоардторемотесессион

Указывает, можно ли синхронизировать локальный буфер обмена с удаленным сеансом.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Параметры

**Значение true** , если локальный буфер обмена можно синхронизировать с удаленным сеансом; в противном случае — **значение false**.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>