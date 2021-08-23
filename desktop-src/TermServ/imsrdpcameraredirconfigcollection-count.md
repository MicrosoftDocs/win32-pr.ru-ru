---
title: Свойство IMsRdpCameraRedirConfigCollection Count
description: Возвращает число объектов Имсрдпкамераредирконфиг в коллекции.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Count
- Свойство Count службы удаленных рабочих столов, интерфейс Имсрдпкамераредирконфигколлектион
- Интерфейс Имсрдпкамераредирконфигколлектион службы удаленных рабочих столов, свойство Count
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8966bcd47793646b678c70eeaf4a263086fb9ced6eb2c56eb7b3821ac3d0f1df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475974"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>Свойство Имсрдпкамераредирконфигколлектион:: count

Возвращает число объектов [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Значение свойства

Число объектов [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекции.

## <a name="requirements"></a>Requirements (Требования)

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