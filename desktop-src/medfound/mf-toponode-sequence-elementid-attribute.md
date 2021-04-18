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
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="9343b-103">\_ \_ \_ Атрибут ELEMENTID топоноде Sequence</span><span class="sxs-lookup"><span data-stu-id="9343b-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="9343b-104">Указывает элемент, содержащий этот исходный узел.</span><span class="sxs-lookup"><span data-stu-id="9343b-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="9343b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9343b-105">Data type</span></span>

<span data-ttu-id="9343b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9343b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9343b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9343b-107">Remarks</span></span>

<span data-ttu-id="9343b-108">Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**).</span><span class="sxs-lookup"><span data-stu-id="9343b-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="9343b-109">В конвейере мультимедиа этот атрибут используется для обнаружения того, когда источники мультимедиа являются частью одного элемента.</span><span class="sxs-lookup"><span data-stu-id="9343b-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="9343b-110">Конвейер обрабатывает все исходные узлы, входящие в один элемент, с одинаковыми часами.</span><span class="sxs-lookup"><span data-stu-id="9343b-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="9343b-111">Когда конвейер помещает в очередь новую топологию, содержащую исходные узлы, которые являются частью элемента, присутствующего в предыдущей топологии, конвейер обрабатывает эти исходные узлы как те же часы, что и исходные узлы из этого элемента в предыдущей топологии.</span><span class="sxs-lookup"><span data-stu-id="9343b-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="9343b-112">В конвейере носителя не указаны неправильные метки времени для исходных узлов с различными тарифами по часам.</span><span class="sxs-lookup"><span data-stu-id="9343b-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="9343b-113">Источник мультимедиа, который может предоставить топологии, должен реализовывать интерфейс [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) или интерфейс [**имфсекуенцерсаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) .</span><span class="sxs-lookup"><span data-stu-id="9343b-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="9343b-114">Источник мультимедиа, предоставляющий топологии, должен задавать атрибут **\_ \_ \_ ELEMENTID топоноде Sequence** для каждого создаваемого исходного узла.</span><span class="sxs-lookup"><span data-stu-id="9343b-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="9343b-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="9343b-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9343b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9343b-116">Requirements</span></span>



| <span data-ttu-id="9343b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9343b-117">Requirement</span></span> | <span data-ttu-id="9343b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9343b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9343b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9343b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9343b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9343b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9343b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9343b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9343b-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9343b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9343b-123">Header</span><span class="sxs-lookup"><span data-stu-id="9343b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9343b-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9343b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9343b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9343b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9343b-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9343b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9343b-127">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="9343b-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9343b-128">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9343b-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9343b-129">**имфмедиасаурцетопологипровидер**</span><span class="sxs-lookup"><span data-stu-id="9343b-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="9343b-130">**имфсекуенцерсаурце**</span><span class="sxs-lookup"><span data-stu-id="9343b-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="9343b-131">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="9343b-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9343b-132">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="9343b-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="9343b-133">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="9343b-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




