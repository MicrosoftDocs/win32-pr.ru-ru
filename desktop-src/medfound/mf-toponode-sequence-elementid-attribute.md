---
description: Указывает элемент, содержащий этот исходный узел.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Атрибут MF_TOPONODE_SEQUENCE_ELEMENTID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00af7212013d26c51ecdf7d2ea4a22855f9b52524c5188d3514d34b5d6976b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739939"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ \_ Атрибут ELEMENTID топоноде Sequence

Указывает элемент, содержащий этот исходный узел.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).

В конвейере мультимедиа этот атрибут используется для обнаружения того, когда источники мультимедиа являются частью одного элемента. Конвейер обрабатывает все исходные узлы, входящие в один элемент, с одинаковыми часами.

Когда конвейер помещает в очередь новую топологию, содержащую исходные узлы, которые являются частью элемента, присутствующего в предыдущей топологии, конвейер обрабатывает эти исходные узлы как те же часы, что и исходные узлы из этого элемента в предыдущей топологии.

> [!Note]  
> В конвейере носителя не указаны неправильные метки времени для исходных узлов с различными тарифами по часам.

 

Источник мультимедиа, который может предоставить топологии, должен реализовывать интерфейс [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) или интерфейс [**имфсекуенцерсаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) . Источник мультимедиа, предоставляющий топологии, должен задавать атрибут **\_ \_ \_ ELEMENTID топоноде Sequence** для каждого создаваемого исходного узла.

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

[**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**имфсекуенцерсаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[Источник Sequencer](sequencer-source.md)
</dt> </dl>

 

 




