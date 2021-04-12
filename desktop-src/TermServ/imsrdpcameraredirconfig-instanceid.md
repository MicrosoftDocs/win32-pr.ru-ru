---
title: Свойство IMsRdpCameraRedirConfig InstanceId
description: Возвращает идентификатор экземпляра камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства InstanceId
- Свойство InstanceId службы удаленных рабочих столов, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство InstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 42654e84f64b25a051a78963339ca95d4ebf760f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104262276"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>Свойство Имсрдпкамераредирконфиг:: InstanceId

Возвращает идентификатор экземпляра камеры.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Значение свойства

Идентификатор экземпляра камеры.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>