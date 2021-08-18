---
description: Указывает, пуста ли текущая топология сегмента.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Атрибут MF_EVENT_SOURCE_FAKE_START (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b026811330443a3fb5e7c9671a7f6a3de8580985b6be4c6ba149a2d4dc196325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973773"
---
# <a name="mf_event_source_fake_start-attribute"></a>\_Источник события \_ MF \_ поддельный \_ атрибут запуска

Указывает, пуста ли текущая топология сегмента.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) .

Источник Sequencer задает для этого атрибута **значение true** , если текущая топология сегмента пуста. Если этот атрибут имеет **значение true**, воспроизведение еще не началось. Значение этого атрибута по умолчанию равно **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




