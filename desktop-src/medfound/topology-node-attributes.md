---
description: Атрибуты узла топологии
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Атрибуты узла топологии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991556"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="24558-103">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="24558-103">Topology Node Attributes</span></span>

<span data-ttu-id="24558-104">Следующие атрибуты применяются к узлам топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="24558-105">Общие атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="24558-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="24558-106">attribute</span><span class="sxs-lookup"><span data-stu-id="24558-106">Attribute</span></span>                                                                       | <span data-ttu-id="24558-107">Описание</span><span class="sxs-lookup"><span data-stu-id="24558-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24558-108">**\_ \_ метод подключения MF \_ топоноде**</span><span class="sxs-lookup"><span data-stu-id="24558-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="24558-109">Указывает, как загрузчик топологии подключает этот узел топологии и является ли этот узел необязательным.</span><span class="sxs-lookup"><span data-stu-id="24558-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="24558-110">**\_декодер MF топоноде \_**</span><span class="sxs-lookup"><span data-stu-id="24558-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="24558-111">Указывает, является ли объект узла топологии декодером.</span><span class="sxs-lookup"><span data-stu-id="24558-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="24558-112">**\_ \_ расшифровка MF топоноде**</span><span class="sxs-lookup"><span data-stu-id="24558-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="24558-113">Указывает, является ли базовый объект узла топологии расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="24558-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="24558-114">**\_ТОПОНОДЕ MF \_**</span><span class="sxs-lookup"><span data-stu-id="24558-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="24558-115">Указывает, может ли конвейер удалять образцы из узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="24558-116">**MF \_ топоноде \_ Ошибка \_ мажортипе**</span><span class="sxs-lookup"><span data-stu-id="24558-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="24558-117">Содержит основной тип носителя для узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="24558-118">Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.</span><span class="sxs-lookup"><span data-stu-id="24558-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="24558-119">**\_ \_ ПОДТИП ошибки MF \_ топоноде**</span><span class="sxs-lookup"><span data-stu-id="24558-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="24558-120">Содержит подтип носителя для узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="24558-121">Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.</span><span class="sxs-lookup"><span data-stu-id="24558-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="24558-122">**\_ \_ код ошибки MF топоноде**</span><span class="sxs-lookup"><span data-stu-id="24558-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="24558-123">Содержит код ошибки последней неудачной попытки подключения для данного узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="24558-124">**MF \_ топоноде \_ заблокировано**</span><span class="sxs-lookup"><span data-stu-id="24558-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="24558-125">Указывает, можно ли изменить типы мультимедиа в этом узле топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="24558-126">**MF \_ топоноде \_ Маркин \_**</span><span class="sxs-lookup"><span data-stu-id="24558-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="24558-127">Указывает, применяет ли конвейер отметку на этом узле.</span><span class="sxs-lookup"><span data-stu-id="24558-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="24558-128">**Разметка MF \_ топоноде \_ \_**</span><span class="sxs-lookup"><span data-stu-id="24558-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="24558-129">Указывает, применяется ли к этому узлу отметка для конвейера.</span><span class="sxs-lookup"><span data-stu-id="24558-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="24558-130">Атрибуты исходного узла</span><span class="sxs-lookup"><span data-stu-id="24558-130">Source Node Attributes</span></span>



| <span data-ttu-id="24558-131">attribute</span><span class="sxs-lookup"><span data-stu-id="24558-131">Attribute</span></span>                                                                                       | <span data-ttu-id="24558-132">Описание</span><span class="sxs-lookup"><span data-stu-id="24558-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24558-133">**MF \_ топоноде \_ медиастарт**</span><span class="sxs-lookup"><span data-stu-id="24558-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="24558-134">Указывает время начала презентации относительно запуска исходного файла мультимедиа в единицах измерения в 100 нс.</span><span class="sxs-lookup"><span data-stu-id="24558-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="24558-135">**MF \_ топоноде \_ медиастоп**</span><span class="sxs-lookup"><span data-stu-id="24558-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="24558-136">Указывает время окончания презентации относительно запуска исходного файла мультимедиа в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="24558-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="24558-137">**\_ \_ дескриптор представления MF \_ топоноде**</span><span class="sxs-lookup"><span data-stu-id="24558-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="24558-138">Содержит указатель на дескриптор представления для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="24558-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="24558-139">**MF \_ топоноде \_ Sequence, пакет \_ ELEMENTID**</span><span class="sxs-lookup"><span data-stu-id="24558-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="24558-140">Указывает элемент, содержащий исходный узел.</span><span class="sxs-lookup"><span data-stu-id="24558-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="24558-141">**\_источник MF топоноде \_**</span><span class="sxs-lookup"><span data-stu-id="24558-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="24558-142">Содержит указатель на источник мультимедиа, связанный с узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="24558-143">**\_ \_ дескриптор потока MF \_ топоноде**</span><span class="sxs-lookup"><span data-stu-id="24558-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="24558-144">Содержит указатель на дескриптор потока для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="24558-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="24558-145">**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**</span><span class="sxs-lookup"><span data-stu-id="24558-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="24558-146">Указывает рабочую очередь для узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="24558-147">**\_ \_ \_ класс MMCSS ТОПОНОДЕ ворккуеуе \_ (MF)**</span><span class="sxs-lookup"><span data-stu-id="24558-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="24558-148">Указывает задачу службы планировщика классов мультимедиа (MMCSS) для узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="24558-149">**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="24558-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="24558-150">Указывает идентификатор задачи MMCSS для узла топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="24558-151">Преобразование атрибутов узла</span><span class="sxs-lookup"><span data-stu-id="24558-151">Transform Node Attributes</span></span>



| <span data-ttu-id="24558-152">attribute</span><span class="sxs-lookup"><span data-stu-id="24558-152">Attribute</span></span>                                                                             | <span data-ttu-id="24558-153">Описание</span><span class="sxs-lookup"><span data-stu-id="24558-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24558-154">**MF \_ топоноде \_ D3DAWARE**</span><span class="sxs-lookup"><span data-stu-id="24558-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="24558-155">Указывает, поддерживает ли преобразование, связанное с узлом топологии, поддержку ускорения видео DirectX (ДКСВА)</span><span class="sxs-lookup"><span data-stu-id="24558-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="24558-156">**\_сток ТОПОНОДЕ \_ MF**</span><span class="sxs-lookup"><span data-stu-id="24558-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="24558-157">Указывает, когда преобразуются преобразования.</span><span class="sxs-lookup"><span data-stu-id="24558-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="24558-158">**\_топоноде \_ запись на диск MF**</span><span class="sxs-lookup"><span data-stu-id="24558-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="24558-159">Указывает, когда преобразование очищается.</span><span class="sxs-lookup"><span data-stu-id="24558-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="24558-160">**\_ИД объекта топоноде для \_ преобразования MF \_**</span><span class="sxs-lookup"><span data-stu-id="24558-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="24558-161">Идентификатор класса (CLSID) преобразования, связанного с этим узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="24558-162">Атрибуты выходного узла</span><span class="sxs-lookup"><span data-stu-id="24558-162">Output Node Attributes</span></span>



| <span data-ttu-id="24558-163">attribute</span><span class="sxs-lookup"><span data-stu-id="24558-163">Attribute</span></span>                                                                                  | <span data-ttu-id="24558-164">Описание</span><span class="sxs-lookup"><span data-stu-id="24558-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24558-165">**MF \_ топоноде \_ Отключить \_ преднакат**</span><span class="sxs-lookup"><span data-stu-id="24558-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="24558-166">Указывает, использует ли сеанс мультимедиа преднакат приемника носителя, представленного этим узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="24558-167">**MF \_ ТОПОНОДЕ \_ Shutdown \_ On \_ Remove**</span><span class="sxs-lookup"><span data-stu-id="24558-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="24558-168">Указывает, завершает ли сеанс мультимедиа приемник мультимедиа при удалении выходного узла из топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="24558-169">**\_топоноде со \_ скоростью MF**</span><span class="sxs-lookup"><span data-stu-id="24558-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="24558-170">Указывает, является ли приемник носителя, связанный с этим узлом топологии, недоступным.</span><span class="sxs-lookup"><span data-stu-id="24558-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="24558-171">**MF \_ топоноде \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="24558-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="24558-172">Идентификатор потока приемника потока, связанного с этим узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="24558-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="24558-173">Атрибуты узла Tee</span><span class="sxs-lookup"><span data-stu-id="24558-173">Tee Node Attributes</span></span>



| <span data-ttu-id="24558-174">attribute</span><span class="sxs-lookup"><span data-stu-id="24558-174">Attribute</span></span>                                                                  | <span data-ttu-id="24558-175">Описание</span><span class="sxs-lookup"><span data-stu-id="24558-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="24558-176">**MF \_ топоноде \_ PRIMARYOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="24558-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="24558-177">Указывает, какие выходные данные являются основными выходными данными на узле Tee.</span><span class="sxs-lookup"><span data-stu-id="24558-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="24558-178">См. также</span><span class="sxs-lookup"><span data-stu-id="24558-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24558-179">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="24558-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="24558-180">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24558-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="24558-181">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="24558-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



