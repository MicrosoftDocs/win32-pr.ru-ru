---
description: Содержит основной тип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Атрибут MF_TOPONODE_ERROR_MAJORTYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711294"
---
# <a name="mf_toponode_error_majortype-attribute"></a><span data-ttu-id="37fce-104">\_Атрибут MF топоноде \_ Error \_ мажортипе</span><span class="sxs-lookup"><span data-stu-id="37fce-104">MF\_TOPONODE\_ERROR\_MAJORTYPE attribute</span></span>

<span data-ttu-id="37fce-105">Содержит основной тип носителя для узла топологии.</span><span class="sxs-lookup"><span data-stu-id="37fce-105">Contains the major media type for a topology node.</span></span> <span data-ttu-id="37fce-106">Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.</span><span class="sxs-lookup"><span data-stu-id="37fce-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="37fce-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="37fce-107">Data type</span></span>

<span data-ttu-id="37fce-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="37fce-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="37fce-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37fce-109">Remarks</span></span>

<span data-ttu-id="37fce-110">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="37fce-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="37fce-111">Загрузчик топологии может задать атрибут.</span><span class="sxs-lookup"><span data-stu-id="37fce-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="37fce-112">Приложения обычно считывают этот атрибут, но не устанавливают его.</span><span class="sxs-lookup"><span data-stu-id="37fce-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="37fce-113">Список возможных значений см. в разделе [основные типы носителей](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="37fce-113">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="37fce-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="37fce-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="37fce-115">Требования</span><span class="sxs-lookup"><span data-stu-id="37fce-115">Requirements</span></span>



| <span data-ttu-id="37fce-116">Требование</span><span class="sxs-lookup"><span data-stu-id="37fce-116">Requirement</span></span> | <span data-ttu-id="37fce-117">Значение</span><span class="sxs-lookup"><span data-stu-id="37fce-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37fce-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37fce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37fce-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37fce-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="37fce-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37fce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37fce-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37fce-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37fce-122">Header</span><span class="sxs-lookup"><span data-stu-id="37fce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37fce-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="37fce-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fce-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37fce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fce-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37fce-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37fce-126">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="37fce-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="37fce-127">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="37fce-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="37fce-128">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="37fce-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="37fce-129">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="37fce-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




