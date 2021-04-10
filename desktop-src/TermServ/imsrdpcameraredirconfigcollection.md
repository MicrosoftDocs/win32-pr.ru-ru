---
title: Интерфейс IMsRdpCameraRedirConfigCollection
description: Представляет коллекцию камер (и связанных конфигураций), доступных для перенаправления.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, описание
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104139174"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>Интерфейс IMsRdpCameraRedirConfigCollection

 Представляет коллекцию камер (и связанных конфигураций), доступных для перенаправления.

## <a name="members"></a>Элементы

Интерфейс **имсрдпкамераредирконфигколлектион** наследует от **IUnknown**. **Имсрдпкамераредирконфигколлектион** также имеет следующие типы членов:

- [Методы](#methods)
- [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **имсрдпкамераредирконфигколлектион** содержит следующие методы.

| Метод            | Описание              |
|:------------------|:-------------------------|
| [**аддконфиг**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Добавляет объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекцию (соответствующая камера не должна быть подключена).                   |
| [**Повторное сканирование**](imsrdpcameraredirconfigcollection-rescan.md)       |  Перечисляет подключенные устройства камеры.                   |

### <a name="properties"></a>Свойства

Интерфейс **имсрдпкамераредирконфигколлектион** имеет следующие свойства.

| Свойство         | Тип доступа           | Описание            |
|:-----------------|:----------------------|:-----------------------|
| [**биндекс**](imsrdpcameraredirconfigcollection-byindex.md)      | Только для чтения |  Возвращает объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) по его индексу в коллекции.   |
| [**бинстанцеид**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Только для чтения |    Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданному идентификатору экземпляра.    |
| [**бисимболиклинк**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Только для чтения |  Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданной символьной ссылке интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.  |
| [**Расчета**](imsrdpcameraredirconfigcollection-count.md)                       | Только для чтения |    Возвращает число объектов [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекции.   |
| [**енкодевидео**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Чтение/запись |  Указывает, является ли поток видео закодированным H. 264.  |
| [**енкодингкуалити**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Чтение/запись |    Задает качество кодирования (скорость потока).   |
| [**редиректбидефаулт**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Чтение/запись |   Указывает, будет ли перенаправлена какая либо новая камера по умолчанию.    |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A            |

## <a name="see-also"></a>См. также раздел

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7:: Камераредирконфигколлектион**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
