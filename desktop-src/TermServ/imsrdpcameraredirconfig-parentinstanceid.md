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
ms.openlocfilehash: 149e4f536996376193596db6c4fd4cf659637c05bb92e3afcdb7ee78c480b893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574564"
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

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|---------------------------------------|
| Минимальная версия клиента| Windows 10, версия 1803 (сборка 17134)      |
| Библиотека типов            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>