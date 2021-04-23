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
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="f5515-103">\_Атрибут с нетопоноденой \_ скоростью MF</span><span class="sxs-lookup"><span data-stu-id="f5515-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="f5515-104">Указывает, является ли приемник носителя, связанный с этим узлом топологии, недоступным.</span><span class="sxs-lookup"><span data-stu-id="f5515-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5515-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f5515-105">Data type</span></span>

<span data-ttu-id="f5515-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f5515-106">**UINT32**</span></span>

<span data-ttu-id="f5515-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f5515-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5515-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5515-108">Remarks</span></span>

<span data-ttu-id="f5515-109">Этот атрибут применяется к выходным узлам **( \_ \_ \_ узел выходных данных топологии MF**).</span><span class="sxs-lookup"><span data-stu-id="f5515-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="f5515-110">Если значение этого атрибута отлично от нуля, сеанс мультимедиа обрабатывает приемник мультимедиа как приемник без учета, независимо от того, возвращает ли приемник носителей характеристику Медиасинк без учета **\_ скорости** .</span><span class="sxs-lookup"><span data-stu-id="f5515-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="f5515-111">Если этот атрибут не задан, приемник мультимедиа предполагается не оценивать.</span><span class="sxs-lookup"><span data-stu-id="f5515-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="f5515-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f5515-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5515-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f5515-113">Requirements</span></span>



| <span data-ttu-id="f5515-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f5515-114">Requirement</span></span> | <span data-ttu-id="f5515-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5515-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5515-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5515-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5515-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5515-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5515-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5515-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5515-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5515-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5515-120">Header</span><span class="sxs-lookup"><span data-stu-id="f5515-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5515-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5515-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5515-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5515-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5515-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5515-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5515-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f5515-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f5515-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f5515-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f5515-126">**Имфмедиасинк:: "характеристики"**</span><span class="sxs-lookup"><span data-stu-id="f5515-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="f5515-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="f5515-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f5515-128">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="f5515-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




