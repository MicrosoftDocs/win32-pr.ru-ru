---
description: Указывает, как сеанс мультимедиа завершает работу объекта в топологии.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Атрибут MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701701"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="996f1-103">MF \_ ТОПОНОДЕ \_ отключение \_ при \_ удалении атрибута</span><span class="sxs-lookup"><span data-stu-id="996f1-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="996f1-104">Указывает, как сеанс мультимедиа завершает работу объекта в топологии.</span><span class="sxs-lookup"><span data-stu-id="996f1-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="996f1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="996f1-105">Data type</span></span>

<span data-ttu-id="996f1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="996f1-106">**UINT32**</span></span>

<span data-ttu-id="996f1-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="996f1-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="996f1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="996f1-108">Remarks</span></span>

<span data-ttu-id="996f1-109">Этот атрибут применяется к следующим типам узлов топологии:</span><span class="sxs-lookup"><span data-stu-id="996f1-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="996f1-110">Выходные узлы</span><span class="sxs-lookup"><span data-stu-id="996f1-110">Output nodes</span></span>
-   <span data-ttu-id="996f1-111">Любой узел преобразования, содержащий *асинхронное* преобразование Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="996f1-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="996f1-112">Атрибут может иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="996f1-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="996f1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="996f1-113">Value</span></span></th>
<th><span data-ttu-id="996f1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="996f1-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="996f1-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="996f1-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="996f1-116">Когда сеанс мультимедиа переключается на новую топологию или очищает текущую топологию, он не завершает работу объекта, принадлежащего этому узлу топологии.</span><span class="sxs-lookup"><span data-stu-id="996f1-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="996f1-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="996f1-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="996f1-118">Когда сеанс мультимедиа переключается на новую топологию или очищает текущую топологию, он завершает работу объекта node следующим образом:</span><span class="sxs-lookup"><span data-stu-id="996f1-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="996f1-119">Выходные узлы. сеанс вызывает <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>имфмедиасинк:: Shutdown</strong></a> в приемнике носителя.</span><span class="sxs-lookup"><span data-stu-id="996f1-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="996f1-120">Узлы преобразования. сеанс вызывает <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>имфшутдовн:: Shutdown</strong></a> в MFT.</span><span class="sxs-lookup"><span data-stu-id="996f1-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="996f1-121">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="996f1-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="996f1-122">Если приложение помещает в очередь несколько топологий, рекомендуется присвоить этому атрибуту значение **false**.</span><span class="sxs-lookup"><span data-stu-id="996f1-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="996f1-123">В противном случае объекты в топологии могут быть неправильно закрыты.</span><span class="sxs-lookup"><span data-stu-id="996f1-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="996f1-124">Этот атрибут не применяется, когда приложение завершает сеанс мультимедиа путем вызова [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="996f1-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="996f1-125">Когда сеанс мультимедиа завершает работу, он всегда завершает работу приемников носителей и асинхронных МФТС в текущей топологии.</span><span class="sxs-lookup"><span data-stu-id="996f1-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="996f1-126">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="996f1-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="996f1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="996f1-127">Requirements</span></span>



| <span data-ttu-id="996f1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="996f1-128">Requirement</span></span> | <span data-ttu-id="996f1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="996f1-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="996f1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="996f1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="996f1-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="996f1-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="996f1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="996f1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="996f1-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="996f1-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="996f1-134">Header</span><span class="sxs-lookup"><span data-stu-id="996f1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="996f1-135"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="996f1-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996f1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="996f1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996f1-137">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="996f1-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="996f1-138">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="996f1-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="996f1-139">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="996f1-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="996f1-140">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="996f1-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="996f1-141">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="996f1-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="996f1-142">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="996f1-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




