---
description: Указывает состояние попытки разрешения топологии.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Атрибут MF_TOPOLOGY_RESOLUTION_STATUS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898346"
---
# <a name="mf_topology_resolution_status-attribute"></a>\_ \_ Атрибут состояния разрешения топологии MF \_

Указывает состояние попытки разрешения топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Загрузчик топологии или сеанс мультимедиа может установить этот атрибут в топологии. Значение этого атрибута является **побитовым** для флагов перечисления [**\_ \_ \_ \_ флагов состояния разрешения топологии MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> </dl>

 

 




