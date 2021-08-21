---
description: Указывает, имеют ли топологии глобальное время начала и окончания.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Атрибут MF_SESSION_GLOBAL_TIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309cc46a070fed571183f7f407e0fb00ad19d4d94136b49a78f0438b21470c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059206"
---
# <a name="mf_session_global_time-attribute"></a>\_ \_ Глобальный \_ атрибут времени сеанса MF

Указывает, имеют ли топологии глобальное время начала и окончания.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут можно задать при создании сесисон мультимедиа с помощью параметра *пконфигуратион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Если этот атрибут существует и имеет ненулевое значение, то все топологии, передаваемые в сеанс мультимедиа, должны иметь атрибуты [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) и [**MF \_ Topology \_ прожектстоп**](mf-topology-projectstop-attribute.md) . Эти атрибуты указывают время начала и окончания топологии относительно всей презентации.

Если этот атрибут отсутствует или **имеет значение false**, топологии не должны иметь атрибут [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) или [**MF \_ Topology \_ прожектстоп**](mf-topology-projectstop-attribute.md) .

Используйте этот атрибут для создания последовательностей редактирования. Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты сеанса мультимедиа](media-session-attributes.md)
</dt> <dt>

[Время представления последовательности](sequence-presentation-times.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**\_прожектстарт топология MF \_**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**\_прожектстоп топология MF \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




