---
title: Метод IMsRdpClipboard SyncRemoteClipboardToLocalSession
description: Синхронизирует удаленный буфер обмена с локальным сеансом.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Синкремотеклипбоардтолокалсессион
- Службы удаленных рабочих столов метода Синкремотеклипбоардтолокалсессион, интерфейс Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, метод Синкремотеклипбоардтолокалсессион
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e1e56a67504ab3182ed6ccaba97591e8259d6e46b6ebdd3bdc06fbaf63c170f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000824"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>Метод Имсрдпклипбоард:: Синкремотеклипбоардтолокалсессион

Синхронизирует удаленный буфер обмена с локальным сеансом.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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