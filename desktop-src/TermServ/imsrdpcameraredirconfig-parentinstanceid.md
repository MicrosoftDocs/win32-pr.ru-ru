---
title: Свойство IMsRdpCameraRedirConfig ParentInstanceId
description: Возвращает идентификатор родительского экземпляра устройства камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Парентинстанцеид
- Службы удаленных рабочих столов свойства Парентинстанцеид, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство Парентинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719224"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>Имсрдпкамераредирконфиг: свойство Арентинстанцеид:P

Возвращает идентификатор родительского экземпляра устройства камеры.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>Значение свойства

Идентификатор родительского экземпляра устройства камеры.

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