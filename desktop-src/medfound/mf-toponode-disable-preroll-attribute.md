---
description: Указывает, использует ли сеанс мультимедиа преднакат приемника носителя, представленного этим узлом топологии.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Атрибут MF_TOPONODE_DISABLE_PREROLL (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647673"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="d2b84-103">MF \_ топоноде \_ Отключить \_ атрибут onрулона</span><span class="sxs-lookup"><span data-stu-id="d2b84-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="d2b84-104">Указывает, использует ли сеанс мультимедиа преднакат приемника носителя, представленного этим узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="d2b84-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2b84-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d2b84-105">Data type</span></span>

<span data-ttu-id="d2b84-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d2b84-106">**UINT32**</span></span>

<span data-ttu-id="d2b84-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="d2b84-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2b84-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2b84-108">Remarks</span></span>

<span data-ttu-id="d2b84-109">Этот атрибут применяется к выходным узлам **( \_ \_ \_ узел выходных данных топологии MF**).</span><span class="sxs-lookup"><span data-stu-id="d2b84-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="d2b84-110">Если значение этого атрибута равно **true**, сеанс мультимедиа не выполняет промежуточную перегрузку данных в приемник мультимедиа, даже если приемник мультимедиа предоставляет интерфейс [**имфмедиасинкпреролл**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="d2b84-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="d2b84-111">Если значение равно **false**, сеанс мультимедиа предмещает данные, если приемник мультимедиа реализует **имфмедиасинкпреролл**.</span><span class="sxs-lookup"><span data-stu-id="d2b84-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="d2b84-112">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d2b84-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="d2b84-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d2b84-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b84-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d2b84-114">Requirements</span></span>



| <span data-ttu-id="d2b84-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d2b84-115">Requirement</span></span> | <span data-ttu-id="d2b84-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d2b84-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b84-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2b84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b84-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2b84-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d2b84-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2b84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b84-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2b84-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d2b84-121">Header</span><span class="sxs-lookup"><span data-stu-id="d2b84-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2b84-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b84-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b84-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2b84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b84-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2b84-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2b84-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="d2b84-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d2b84-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d2b84-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d2b84-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="d2b84-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d2b84-128">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="d2b84-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




