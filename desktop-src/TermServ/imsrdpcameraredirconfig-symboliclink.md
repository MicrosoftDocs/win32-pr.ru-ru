---
title: Свойство IMsRdpCameraRedirConfig SymbolicLink
description: Возвращает символьную ссылку интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства SymbolicLink
- Службы удаленных рабочих столов свойства SymbolicLink, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "103894010"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>Свойство Имсрдпкамераредирконфиг:: SymbolicLink

Возвращает символьную ссылку интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>Значение свойства

Символьная ссылка на интерфейс **KSCATEGORY_VIDEO_CAMERA** для камеры.

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