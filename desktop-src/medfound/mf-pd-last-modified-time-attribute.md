---
description: Указывает время последнего изменения презентации.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: Атрибут MF_PD_LAST_MODIFIED_TIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998851"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="e0575-103">\_ \_ \_ Атрибут времени последнего изменения MF PD \_</span><span class="sxs-lookup"><span data-stu-id="e0575-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="e0575-104">Указывает время последнего изменения презентации.</span><span class="sxs-lookup"><span data-stu-id="e0575-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0575-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e0575-105">Data type</span></span>

<span data-ttu-id="e0575-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="e0575-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="e0575-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0575-107">Remarks</span></span>

<span data-ttu-id="e0575-108">Источники мультимедиа могут задавать этот атрибут для дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="e0575-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="e0575-109">Значением атрибута является структура **fileTime** , которая описана в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e0575-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="e0575-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="e0575-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0575-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e0575-111">Requirements</span></span>



| <span data-ttu-id="e0575-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e0575-112">Requirement</span></span> | <span data-ttu-id="e0575-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e0575-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0575-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0575-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e0575-115">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="e0575-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e0575-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0575-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e0575-117">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="e0575-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e0575-118">Header</span><span class="sxs-lookup"><span data-stu-id="e0575-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0575-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0575-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0575-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0575-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0575-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0575-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0575-122">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="e0575-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="e0575-123">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="e0575-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="e0575-124">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="e0575-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="e0575-125">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="e0575-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




