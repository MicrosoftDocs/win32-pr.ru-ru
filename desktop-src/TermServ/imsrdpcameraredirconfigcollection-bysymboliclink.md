---
title: Свойство IMsRdpCameraRedirConfigCollection BySymbolicLink
description: Возвращает из коллекции объект Имсрдпкамераредирконфиг, соответствующий заданной символьной ссылке интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Бисимболиклинк
- Службы удаленных рабочих столов свойства Бисимболиклинк, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Бисимболиклинк
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719220"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>Имсрдпкамераредирконфигколлектион::. Бисимболиклинк, свойство

Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданной символьной ссылке интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Значение свойства

Объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий указанной символической ссылке.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>