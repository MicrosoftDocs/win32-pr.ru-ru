---
description: Содержит указатель на прокси-объект для дескриптора представления приложений.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: Атрибут MF_PD_PMPHOST_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423973"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="e3b74-103">\_ \_ Атрибут контекста MF PD пмфост \_</span><span class="sxs-lookup"><span data-stu-id="e3b74-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="e3b74-104">Содержит указатель на прокси-объект для дескриптора представления приложения.</span><span class="sxs-lookup"><span data-stu-id="e3b74-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3b74-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e3b74-105">Data type</span></span>

<span data-ttu-id="e3b74-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e3b74-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b74-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3b74-107">Remarks</span></span>

<span data-ttu-id="e3b74-108">Узел защищенного пути к носителю (PMP) использует этот атрибут для хранения дескриптора представления приложения в дескрипторе удаленной презентации.</span><span class="sxs-lookup"><span data-stu-id="e3b74-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="e3b74-109">Значение атрибута является указателем на интерфейс [_ *имфремотепрокси* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .</span><span class="sxs-lookup"><span data-stu-id="e3b74-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="e3b74-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="e3b74-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b74-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e3b74-111">Requirements</span></span>



| <span data-ttu-id="e3b74-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e3b74-112">Requirement</span></span> | <span data-ttu-id="e3b74-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e3b74-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b74-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3b74-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b74-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3b74-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e3b74-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3b74-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b74-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3b74-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3b74-118">Header</span><span class="sxs-lookup"><span data-stu-id="e3b74-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3b74-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b74-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b74-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3b74-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b74-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3b74-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3b74-122">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="e3b74-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="e3b74-123">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="e3b74-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="e3b74-124">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="e3b74-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="e3b74-125">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="e3b74-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




