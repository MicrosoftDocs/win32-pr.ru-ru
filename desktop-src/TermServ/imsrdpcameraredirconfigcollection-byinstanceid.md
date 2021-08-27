---
title: Свойство IMsRdpCameraRedirConfigCollection ByInstanceId
description: Возвращает из коллекции объект Имсрдпкамераредирконфиг, соответствующий заданному ИДЕНТИФИКАТОРу экземпляра.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Бинстанцеид
- Службы удаленных рабочих столов свойства Бинстанцеид, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Бинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e621efa61c6e033a9066da30fc6a2a97c76ebec94e9bfe848743f8b031b08d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080074"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>Свойство Имсрдпкамераредирконфигколлектион:: Бинстанцеид

Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданному идентификатору экземпляра.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Значение свойства

Объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданному идентификатору экземпляра.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>