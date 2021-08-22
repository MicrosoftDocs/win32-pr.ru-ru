---
description: Указывает, можно ли изменить типы мультимедиа в этом узле топологии.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: Атрибут MF_TOPONODE_LOCKED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2158a44480fa2b4e884cc2e700e8f479b4af042907e351b26bc5704d7fc20fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119356274"
---
# <a name="mf_toponode_locked-attribute"></a>\_Атрибут MF топоноде \_ locked

Указывает, можно ли изменить типы мультимедиа в этом узле топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут применяется ко всем типам узлов.

Если значение этого атрибута отлично от нуля, то загрузчик топологии не изменит типы носителей. Этот атрибут имеет значение **true** , если узел используется.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




