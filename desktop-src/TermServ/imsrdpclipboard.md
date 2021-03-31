---
title: Интерфейс IMsRdpClipboard
description: Представляет контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, описание
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104139186"
---
# <a name="imsrdpclipboard-interface"></a>Интерфейс IMsRdpClipboard

Представляет контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена (то есть для свойства [мануалклипбоардсинценаблед](imsrdpextendedsettings-property.md) задано значение **true**).

## <a name="members"></a>Элементы

Интерфейс **имсрдпклипбоард** наследует от **IUnknown**. **Имсрдпклипбоард** также имеет следующие типы членов:

- [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **имсрдпклипбоард** содержит следующие методы.


| Метод        | Описание      |
|:---------------|:----------------|
| [**кансинклокалклипбоардторемотесессион**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Указывает, можно ли синхронизировать локальный буфер обмена с удаленным сеансом.                   |
| [**кансинкремотеклипбоардтолокалсессион**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Указывает, можно ли синхронизировать удаленный буфер обмена с локальным сеансом.                   |
| [**синклокалклипбоардторемотесессион**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Синхронизирует локальный буфер обмена с удаленным сеансом.                   |
| [**синкремотеклипбоардтолокалсессион**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Синхронизирует удаленный буфер обмена с локальным сеансом.                      |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable7:: Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
