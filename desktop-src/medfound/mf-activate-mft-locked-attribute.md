---
description: Указывает, будет ли загрузчик топологии изменять типы носителей на Media Foundation преобразовании (MFT). Приложения обычно не используют этот атрибут.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Атрибут MF_ACTIVATE_MFT_LOCKED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155571"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="8b1df-104">MF \_ Активация \_ \_ атрибута MFT locked</span><span class="sxs-lookup"><span data-stu-id="8b1df-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="8b1df-105">Указывает, будет ли загрузчик топологии изменять типы носителей на Media Foundation преобразовании (MFT).</span><span class="sxs-lookup"><span data-stu-id="8b1df-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="8b1df-106">Приложения обычно не используют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="8b1df-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b1df-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8b1df-107">Data type</span></span>

<span data-ttu-id="8b1df-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b1df-108">**UINT32**</span></span>

<span data-ttu-id="8b1df-109">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="8b1df-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b1df-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b1df-110">Remarks</span></span>

<span data-ttu-id="8b1df-111">Если значение этого атрибута отлично от нуля, то загрузчик топологии не изменит типы носителей в MFT.</span><span class="sxs-lookup"><span data-stu-id="8b1df-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="8b1df-112">Загрузчик топологии задает этот атрибут после загрузки топологии.</span><span class="sxs-lookup"><span data-stu-id="8b1df-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="8b1df-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="8b1df-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1df-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8b1df-114">Requirements</span></span>



| <span data-ttu-id="8b1df-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8b1df-115">Requirement</span></span> | <span data-ttu-id="8b1df-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8b1df-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1df-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b1df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1df-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b1df-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b1df-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b1df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1df-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b1df-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8b1df-121">Header</span><span class="sxs-lookup"><span data-stu-id="8b1df-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b1df-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b1df-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1df-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b1df-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1df-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b1df-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b1df-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b1df-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8b1df-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8b1df-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8b1df-127">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="8b1df-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




