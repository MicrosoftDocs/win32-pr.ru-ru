---
description: Содержит указатель на дескриптор представления из защищенного пути к носителю (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Атрибут MF_PD_APP_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266020"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="13c84-103">\_ \_ Атрибут контекста приложения MF PD \_</span><span class="sxs-lookup"><span data-stu-id="13c84-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="13c84-104">Содержит указатель на дескриптор представления из защищенного пути к носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="13c84-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="13c84-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="13c84-105">Data type</span></span>

<span data-ttu-id="13c84-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="13c84-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="13c84-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13c84-107">Remarks</span></span>

<span data-ttu-id="13c84-108">Прокси-сервер источника мультимедиа, созданный в процессе PMP, использует этот атрибут для хранения дескриптора удаленной презентации в дескрипторе представления приложения.</span><span class="sxs-lookup"><span data-stu-id="13c84-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="13c84-109">Значение этого атрибута является указателем на интерфейс [_ *имфпресентатиондескриптор* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="13c84-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="13c84-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="13c84-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c84-111">Требования</span><span class="sxs-lookup"><span data-stu-id="13c84-111">Requirements</span></span>



| <span data-ttu-id="13c84-112">Требование</span><span class="sxs-lookup"><span data-stu-id="13c84-112">Requirement</span></span> | <span data-ttu-id="13c84-113">Значение</span><span class="sxs-lookup"><span data-stu-id="13c84-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13c84-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13c84-114">Minimum supported client</span></span><br/> | <span data-ttu-id="13c84-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13c84-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="13c84-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13c84-116">Minimum supported server</span></span><br/> | <span data-ttu-id="13c84-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13c84-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="13c84-118">Header</span><span class="sxs-lookup"><span data-stu-id="13c84-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c84-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c84-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c84-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13c84-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c84-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13c84-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="13c84-122">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="13c84-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="13c84-123">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="13c84-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="13c84-124">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="13c84-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




