---
description: Содержит отображаемое имя для аппаратного преобразования Media Foundation (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Атрибут MFT_FRIENDLY_NAME_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647273"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="0a3d2-103">\_ \_ Атрибут атрибута понятного имени MFT \_</span><span class="sxs-lookup"><span data-stu-id="0a3d2-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="0a3d2-104">Содержит отображаемое имя для аппаратного преобразования Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="0a3d2-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="0a3d2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0a3d2-105">Data type</span></span>

<span data-ttu-id="0a3d2-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="0a3d2-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="0a3d2-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="0a3d2-107">Get/set</span></span>

<span data-ttu-id="0a3d2-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="0a3d2-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="0a3d2-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="0a3d2-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a3d2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a3d2-110">Remarks</span></span>

<span data-ttu-id="0a3d2-111">Этот атрибут поддерживается МФТС на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="0a3d2-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="0a3d2-112">Он также задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , выделенных функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , если эти указатели представляют аппаратную МФТС.</span><span class="sxs-lookup"><span data-stu-id="0a3d2-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="0a3d2-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="0a3d2-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3d2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0a3d2-114">Requirements</span></span>



| <span data-ttu-id="0a3d2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0a3d2-115">Requirement</span></span> | <span data-ttu-id="0a3d2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0a3d2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3d2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a3d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a3d2-118">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="0a3d2-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0a3d2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a3d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a3d2-120">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0a3d2-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0a3d2-121">Header</span><span class="sxs-lookup"><span data-stu-id="0a3d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a3d2-122"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a3d2-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a3d2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a3d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3d2-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a3d2-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a3d2-125">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="0a3d2-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




