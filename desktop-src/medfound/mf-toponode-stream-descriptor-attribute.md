---
description: Содержит указатель на дескриптор потока для источника мультимедиа.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Атрибут MF_TOPONODE_STREAM_DESCRIPTOR (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701699"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>\_ \_ \_ Атрибут дескриптора потока MF топоноде

Содержит указатель на дескриптор потока для источника мультимедиа.

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к исходным узлам (_ * MF \_ TOPOLOGY \_ саурцестреам \_ node * *).

Значение атрибута является указателем на интерфейс [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) дескриптора потока. Атрибут обязателен.

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

[**Имфаттрибутес:: неизвестный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Имфаттрибутес:: Сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




