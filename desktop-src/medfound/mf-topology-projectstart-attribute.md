---
description: Задает время окончания топологии относительно начала первой топологии в последовательности.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Атрибут MF_TOPOLOGY_PROJECTSTART (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898349"
---
# <a name="mf_topology_projectstart-attribute"></a>\_ \_ Атрибут ПРОЖЕКТСТАРТ топологии MF

Задает время окончания топологии относительно начала первой топологии в последовательности.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Комментарии

Значение задается в единицах 100 наносекунд.

Если сеанс мультимедиа был создан с атрибутом [**\_ \_ глобального \_ времени сеанса MF**](mf-session-global-time-attribute.md) , равным **true**, все топологии должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстарт** . В противном случае топологии не должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстарт** . Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Время представления последовательности](sequence-presentation-times.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_прожектстоп топология MF \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




