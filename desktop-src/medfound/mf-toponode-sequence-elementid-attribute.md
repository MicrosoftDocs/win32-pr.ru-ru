---
description: Указывает элемент, содержащий этот исходный узел.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Атрибут MF_TOPONODE_SEQUENCE_ELEMENTID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711285"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ \_ Атрибут ELEMENTID топоноде Sequence

Указывает элемент, содержащий этот исходный узел.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).

В конвейере мультимедиа этот атрибут используется для обнаружения того, когда источники мультимедиа являются частью одного элемента. Конвейер обрабатывает все исходные узлы, входящие в один элемент, с одинаковыми часами.

Когда конвейер помещает в очередь новую топологию, содержащую исходные узлы, которые являются частью элемента, присутствующего в предыдущей топологии, конвейер обрабатывает эти исходные узлы как те же часы, что и исходные узлы из этого элемента в предыдущей топологии.

> [!Note]  
> В конвейере носителя не указаны неправильные метки времени для исходных узлов с различными тарифами по часам.

 

Источник мультимедиа, который может предоставить топологии, должен реализовывать интерфейс [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) или интерфейс [**имфсекуенцерсаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) . Источник мультимедиа, предоставляющий топологии, должен задавать атрибут **\_ \_ \_ ELEMENTID топоноде Sequence** для каждого создаваемого исходного узла.

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

 

 




