---
description: Задает время начала для топологии относительно начала первой топологии в последовательности.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: Атрибут MF_TOPOLOGY_PROJECTSTOP (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544335"
---
# <a name="mf_topology_projectstop-attribute"></a>\_ \_ Атрибут ПРОЖЕКТСТОП топологии MF

Задает время начала для топологии относительно начала первой топологии в последовательности.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="remarks"></a>Комментарии

Значение задается в единицах 100 наносекунд.

Если сеанс мультимедиа был создан с атрибутом [**\_ \_ глобального \_ времени сеанса MF**](mf-session-global-time-attribute.md) , равным **true**, все топологии должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстоп** . В противном случае топологии не должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстоп** . Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).

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

[**\_прожектстарт топология MF \_**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




