---
description: Указывает, является ли приемник носителя, связанный с этим узлом топологии, недоступным.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: Атрибут MF_TOPONODE_RATELESS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711284"
---
# <a name="mf_toponode_rateless-attribute"></a>\_Атрибут с нетопоноденой \_ скоростью MF

Указывает, является ли приемник носителя, связанный с этим узлом топологии, недоступным.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к выходным узлам **( \_ \_ \_ узел выходных данных топологии MF**).

Если значение этого атрибута отлично от нуля, сеанс мультимедиа обрабатывает приемник мультимедиа как приемник без учета, независимо от того, возвращает ли приемник носителей характеристику Медиасинк без учета **\_ скорости** . Если этот атрибут не задан, приемник мультимедиа предполагается не оценивать.

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

[**Имфмедиасинк:: "характеристики"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




