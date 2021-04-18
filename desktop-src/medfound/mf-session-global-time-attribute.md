---
description: Указывает, имеют ли топологии глобальное время начала и окончания.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Атрибут MF_SESSION_GLOBAL_TIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712323"
---
# <a name="mf_session_global_time-attribute"></a>\_ \_ Глобальный \_ атрибут времени сеанса MF

Указывает, имеют ли топологии глобальное время начала и окончания.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут можно задать при создании сесисон мультимедиа с помощью параметра *пконфигуратион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Если этот атрибут существует и имеет ненулевое значение, то все топологии, передаваемые в сеанс мультимедиа, должны иметь атрибуты [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) и [**MF \_ Topology \_ прожектстоп**](mf-topology-projectstop-attribute.md) . Эти атрибуты указывают время начала и окончания топологии относительно всей презентации.

Если этот атрибут отсутствует или **имеет значение false**, топологии не должны иметь атрибут [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) или [**MF \_ Topology \_ прожектстоп**](mf-topology-projectstop-attribute.md) .

Используйте этот атрибут для создания последовательностей редактирования. Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).

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

 

 




