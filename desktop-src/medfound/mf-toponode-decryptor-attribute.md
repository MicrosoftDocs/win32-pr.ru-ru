---
description: Указывает, является ли базовый объект топологии узлами дешифрованием.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Атрибут MF_TOPONODE_DECRYPTOR (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703077"
---
# <a name="mf_toponode_decryptor-attribute"></a>\_ \_ Атрибут расшифровки MF топоноде

Указывает, является ли базовый объект узла топологии расшифровывается.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут применяется ко всем типам узлов.

Если значение этого атрибута не равно нулю, то базовый объект узла является расшифрованным.

Обычно приложения не используют этот атрибут напрямую. Сеанс мультимедиа задает этот атрибут при создании узла для расшифровки, полученного из метода [**имфинпуттрустаусорити::-дешифратора**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .

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

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




