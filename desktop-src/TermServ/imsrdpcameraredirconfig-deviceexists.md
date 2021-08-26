---
title: Свойство IMsRdpCameraRedirConfig DeviceExists
description: Указывает, существует ли устройство камеры (т. е. Камера подключено).
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицеексистс
- Службы удаленных рабочих столов свойства Девицеексистс, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство Девицеексистс
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 617c91491d88736ca60218d71f9dd5aa02ad0f9faeefdda6b872ba9262cec587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990664"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>Имсрдпкамераредирконфиг: свойство Евицеексистс:D

Указывает, существует ли устройство камеры (т. е. Камера подключено).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Значение свойства

Значение, указывающее, существует ли устройство камеры в данный момент (то есть подключение камеры).

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