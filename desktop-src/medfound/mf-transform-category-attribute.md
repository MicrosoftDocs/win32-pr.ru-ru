---
description: Указывает категорию Media Foundation преобразования (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Атрибут MF_TRANSFORM_CATEGORY_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263356"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="6e575-103">\_ \_ Атрибут атрибута категории для преобразования MF \_</span><span class="sxs-lookup"><span data-stu-id="6e575-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="6e575-104">Указывает категорию Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="6e575-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="6e575-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6e575-105">Data type</span></span>

<span data-ttu-id="6e575-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="6e575-106">**GUID**</span></span>

<span data-ttu-id="6e575-107">Список возможных значений см. в разделе [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="6e575-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="6e575-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="6e575-108">Get/set</span></span>

<span data-ttu-id="6e575-109">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.</span><span class="sxs-lookup"><span data-stu-id="6e575-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="6e575-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="6e575-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e575-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e575-111">Remarks</span></span>

<span data-ttu-id="6e575-112">Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="6e575-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e575-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6e575-113">Requirements</span></span>



| <span data-ttu-id="6e575-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6e575-114">Requirement</span></span> | <span data-ttu-id="6e575-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6e575-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e575-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e575-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e575-117">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="6e575-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6e575-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e575-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e575-119">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="6e575-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6e575-120">Header</span><span class="sxs-lookup"><span data-stu-id="6e575-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e575-121"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e575-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e575-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e575-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e575-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e575-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e575-124">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="6e575-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




