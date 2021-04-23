---
description: Определяет узел топологии для приемника потока.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Атрибут MF_EVENT_OUTPUT_NODE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656580"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="4eb01-103">\_ \_ Атрибут узла вывода события MF \_</span><span class="sxs-lookup"><span data-stu-id="4eb01-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="4eb01-104">Определяет узел топологии для приемника потока.</span><span class="sxs-lookup"><span data-stu-id="4eb01-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="4eb01-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4eb01-105">Data type</span></span>

<span data-ttu-id="4eb01-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4eb01-106">**UINT64**</span></span>

<span data-ttu-id="4eb01-107">Рассматривать как [**топоид**](topoid.md).</span><span class="sxs-lookup"><span data-stu-id="4eb01-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb01-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4eb01-108">Remarks</span></span>

<span data-ttu-id="4eb01-109">Значение этого атрибута является идентификатором узла для выходного узла в текущей топологии.</span><span class="sxs-lookup"><span data-stu-id="4eb01-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="4eb01-110">Чтобы получить указатель на связанный узел, вызовите [**имфтопологи:: жетнодебид**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) в топологии.</span><span class="sxs-lookup"><span data-stu-id="4eb01-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="4eb01-111">Этот атрибут используется со следующими событиями:</span><span class="sxs-lookup"><span data-stu-id="4eb01-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="4eb01-112">месессионстреамсинкформатчанжед</span><span class="sxs-lookup"><span data-stu-id="4eb01-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="4eb01-113">месинкинвалидатед</span><span class="sxs-lookup"><span data-stu-id="4eb01-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="4eb01-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4eb01-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb01-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4eb01-115">Requirements</span></span>



| <span data-ttu-id="4eb01-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4eb01-116">Requirement</span></span> | <span data-ttu-id="4eb01-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4eb01-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb01-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eb01-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb01-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4eb01-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4eb01-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eb01-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb01-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4eb01-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4eb01-122">Header</span><span class="sxs-lookup"><span data-stu-id="4eb01-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb01-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb01-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb01-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eb01-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb01-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4eb01-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4eb01-126">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="4eb01-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4eb01-127">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="4eb01-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="4eb01-128">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="4eb01-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




