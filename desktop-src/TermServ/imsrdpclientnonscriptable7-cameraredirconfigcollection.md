---
title: Свойство IMsRdpClientNonScriptable7 CameraRedirConfigCollection
description: Возвращает коллекцию камер (и связанных конфигураций), доступных для перенаправления.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Камераредирконфигколлектион
- Службы удаленных рабочих столов свойства Камераредирконфигколлектион, интерфейс IMsRdpClientNonScriptable7
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7, свойство Камераредирконфигколлектион
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341395"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>Свойство IMsRdpClientNonScriptable7:: Камераредирконфигколлектион

Возвращает коллекцию камер (и связанных конфигураций), доступных для перенаправления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Значение свойства

Объект [имсрдпкамераредирконфигколлектион](imsrdpcameraredirconfigcollection.md) , представляющий коллекцию камер (и связанных конфигураций), которые доступны для перенаправления.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 определен как 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>