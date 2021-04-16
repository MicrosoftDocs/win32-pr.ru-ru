---
title: Интерфейс IMsRdpCameraRedirConfig
description: Представляет конфигурации для камеры, доступной для перенаправления.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, описание
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536383"
---
# <a name="imsrdpcameraredirconfig-interface"></a>Интерфейс IMsRdpCameraRedirConfig

Представляет конфигурации для камеры, доступной для перенаправления.

## <a name="members"></a>Элементы

Интерфейс **имсрдпкамераредирконфиг** наследует от **IUnknown**. **Имсрдпкамераредирконфиг** также имеет следующие типы членов:

- [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **имсрдпкамераредирконфиг** имеет следующие свойства.

| Свойство         | Тип доступа           | Описание            |
|:-----------------|:----------------------|:-----------------------|
| [**девицеексистс**](imsrdpcameraredirconfig-deviceexists.md)      | Только для чтения | Указывает, существует ли устройство камеры (т. е. Камера подключено).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Только для чтения |    Возвращает понятное имя камеры.    |
| [**InstanceId**](imsrdpcameraredirconfig-instanceid.md)      | Только для чтения |  Возвращает идентификатор экземпляра камеры.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Только для чтения |    Возвращает идентификатор родительского экземпляра устройства камеры.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Чтение/запись |  Указывает, будет ли перенаправлена камера.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Только для чтения |   Возвращает символьную ссылку интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.   |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>См. также раздел

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7:: Камераредирконфигколлектион**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)