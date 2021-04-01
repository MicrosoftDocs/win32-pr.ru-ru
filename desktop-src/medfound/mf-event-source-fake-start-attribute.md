---
description: Указывает, пуста ли текущая топология сегмента.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Атрибут MF_EVENT_SOURCE_FAKE_START (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913736"
---
# <a name="mf_event_source_fake_start-attribute"></a>\_Источник события \_ MF \_ поддельный \_ атрибут запуска

Указывает, пуста ли текущая топология сегмента.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) .

Источник Sequencer задает для этого атрибута **значение true** , если текущая топология сегмента пуста. Если этот атрибут имеет **значение true**, воспроизведение еще не началось. Значение этого атрибута по умолчанию равно **false**.

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

 

 




