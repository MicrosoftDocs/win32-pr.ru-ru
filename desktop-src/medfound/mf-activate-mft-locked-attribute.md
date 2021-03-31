---
description: Указывает, будет ли загрузчик топологии изменять типы носителей на Media Foundation преобразовании (MFT). Приложения обычно не используют этот атрибут.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Атрибут MF_ACTIVATE_MFT_LOCKED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155571"
---
# <a name="mf_activate_mft_locked-attribute"></a>MF \_ Активация \_ \_ атрибута MFT locked

Указывает, будет ли загрузчик топологии изменять типы носителей на Media Foundation преобразовании (MFT). Приложения обычно не используют этот атрибут.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Если значение этого атрибута отлично от нуля, то загрузчик топологии не изменит типы носителей в MFT. Загрузчик топологии задает этот атрибут после загрузки топологии.

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

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




