---
description: Указывает, будет ли загрузчик топологии изменять типы носителей на Media Foundation преобразовании (MFT). Приложения обычно не используют этот атрибут.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Атрибут MF_ACTIVATE_MFT_LOCKED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060914"
---
# <a name="mf_activate_mft_locked-attribute"></a>MF \_ Активация \_ \_ атрибута MFT locked

Указывает, будет ли загрузчик топологии изменять типы носителей на Media Foundation преобразовании (MFT). Приложения обычно не используют этот атрибут.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Если значение этого атрибута отлично от нуля, то загрузчик топологии не изменит типы носителей в MFT. Загрузчик топологии задает этот атрибут после загрузки топологии.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




