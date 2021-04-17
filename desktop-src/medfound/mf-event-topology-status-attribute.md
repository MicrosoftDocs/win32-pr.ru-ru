---
description: Указывает состояние топологии во время воспроизведения.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: Атрибут MF_EVENT_TOPOLOGY_STATUS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693770"
---
# <a name="mf_event_topology_status-attribute"></a>\_ \_ Атрибут состояния ТОПОЛОГИИ событий MF \_

Указывает состояние топологии во время воспроизведения.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является членом перечисления [**MF \_ топостатус**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) .

Этот атрибут используется с событием [месессионтопологистатус](mesessiontopologystatus.md) .

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

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




