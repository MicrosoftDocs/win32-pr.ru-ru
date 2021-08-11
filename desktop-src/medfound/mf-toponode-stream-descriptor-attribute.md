---
description: Содержит указатель на дескриптор потока для источника мультимедиа.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Атрибут MF_TOPONODE_STREAM_DESCRIPTOR (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92517560f0a1f60681afc1209d6d14d3e3c5d663958d365d18b20558c0003199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244328"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>\_ \_ \_ Атрибут дескриптора потока MF топоноде

Содержит указатель на дескриптор потока для источника мультимедиа.

## <a name="data-type"></a>Тип данных

**IUnknown\***

## <a name="remarks"></a>Remarks

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).

Значение атрибута является указателем на интерфейс [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) дескриптора потока. Атрибут обязателен.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

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

 

 




