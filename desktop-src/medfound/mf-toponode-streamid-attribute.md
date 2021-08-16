---
description: Идентификатор потока приемника потока, связанного с этим узлом топологии.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: Атрибут MF_TOPONODE_STREAMID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cf1edc8918af91144de4f408e7913c3f40b1f0246059bc5bf9e4f1193a1cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739893"
---
# <a name="mf_toponode_streamid-attribute"></a>\_Атрибут MF топоноде \_ STREAMID

Идентификатор потока приемника потока, связанного с этим узлом топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к выходным узлам **( \_ \_ \_ узел выходных данных топологии MF**).

Когда сеанс мультимедиа загружает топологию, он запрашивает приемник потока, используя указанный идентификатор. В случае сбоя он пытается добавить новый приемник потока в приемник мультимедиа.

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

 

 




