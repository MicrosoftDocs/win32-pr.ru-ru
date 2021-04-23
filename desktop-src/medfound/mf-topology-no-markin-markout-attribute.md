---
description: Указывает, обрезает ли образцы в конвейере.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Атрибут MF_TOPOLOGY_NO_MARKIN_MARKOUT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263617"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="4a460-103">\_Топология \_ MF \_ отсутствует \_ атрибут Маркин Mark</span><span class="sxs-lookup"><span data-stu-id="4a460-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="4a460-104">Указывает, обрезает ли образцы в конвейере.</span><span class="sxs-lookup"><span data-stu-id="4a460-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a460-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4a460-105">Data type</span></span>

<span data-ttu-id="4a460-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a460-106">**UINT32**</span></span>

<span data-ttu-id="4a460-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="4a460-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a460-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a460-108">Remarks</span></span>

<span data-ttu-id="4a460-109">По умолчанию конвейер обрезает образцы в соответствии с правильным временем представления.</span><span class="sxs-lookup"><span data-stu-id="4a460-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="4a460-110">Усечение выполняется на узлах топологии с атрибутами [**MF \_ топоноде \_ Маркин \_ здесь**](mf-toponode-markin-here-attribute.md) и [**MF \_ топоноде \_ меток \_**](mf-toponode-markout-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4a460-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="4a460-111">Если **для топологии** **MF не задан атрибут \_ \_ \_ Маркин \_ Mark** , то конвейер не усекает выборки, а **MF \_ топоноде \_ Маркин \_ здесь** и **MF топоноде. \_ \_ \_ здесь** атрибуты игнорируются.</span><span class="sxs-lookup"><span data-stu-id="4a460-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="4a460-112">Если атрибут не задан или имеет значение **false**, конвейер усекает выборки.</span><span class="sxs-lookup"><span data-stu-id="4a460-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="4a460-113">Приложение может задать для параметра **" \_ топология MF \_ No \_ Маркин \_ Mark** " **значение true** , если приложение получает сжатые образцы из конвейера и должно получить все ключевые кадры, которые в противном случае могут быть обрезаны.</span><span class="sxs-lookup"><span data-stu-id="4a460-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="4a460-114">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="4a460-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="4a460-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4a460-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a460-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4a460-116">Requirements</span></span>



| <span data-ttu-id="4a460-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4a460-117">Requirement</span></span> | <span data-ttu-id="4a460-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4a460-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a460-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a460-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a460-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a460-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a460-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a460-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a460-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a460-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a460-123">Header</span><span class="sxs-lookup"><span data-stu-id="4a460-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a460-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a460-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a460-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a460-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a460-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a460-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a460-127">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a460-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4a460-128">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4a460-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4a460-129">**MF \_ топоноде \_ Маркин \_**</span><span class="sxs-lookup"><span data-stu-id="4a460-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="4a460-130">**Разметка MF \_ топоноде \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a460-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="4a460-131">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="4a460-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




