---
description: Содержит символьную ссылку для преобразования Media Foundation на основе оборудования (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Атрибут MFT_ENUM_HARDWARE_URL_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263896"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="9537e-103">\_ \_ \_ Атрибут атрибута аппаратного URL-адреса перечисления MFT \_</span><span class="sxs-lookup"><span data-stu-id="9537e-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="9537e-104">Содержит символьную ссылку для преобразования Media Foundation на основе оборудования (MFT).</span><span class="sxs-lookup"><span data-stu-id="9537e-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="9537e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9537e-105">Data type</span></span>

<span data-ttu-id="9537e-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9537e-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="9537e-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="9537e-107">Get/set</span></span>

<span data-ttu-id="9537e-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="9537e-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="9537e-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="9537e-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="9537e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9537e-110">Remarks</span></span>

<span data-ttu-id="9537e-111">Этот атрибут поддерживается МФТС на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="9537e-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="9537e-112">Значение атрибута является символьной ссылкой для драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="9537e-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="9537e-113">Этот атрибут также задается в [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателях, выделенных функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , если эти указатели представляют аппаратное МФТС.</span><span class="sxs-lookup"><span data-stu-id="9537e-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="9537e-114">Символьная ссылка должна рассматриваться как непрозрачная строка.</span><span class="sxs-lookup"><span data-stu-id="9537e-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="9537e-115">Чтобы получить отображаемое имя для устройства, запросите [атрибут \_ понятного \_ имени MFT](mft-friendly-name-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9537e-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="9537e-116">Для программного МФТС не должен быть задан этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="9537e-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="9537e-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="9537e-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9537e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9537e-118">Requirements</span></span>



| <span data-ttu-id="9537e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9537e-119">Requirement</span></span> | <span data-ttu-id="9537e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9537e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9537e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9537e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9537e-122">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="9537e-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9537e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9537e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9537e-124">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9537e-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9537e-125">Header</span><span class="sxs-lookup"><span data-stu-id="9537e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9537e-126"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="9537e-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9537e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9537e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9537e-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9537e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9537e-129">Оборудование МФТС</span><span class="sxs-lookup"><span data-stu-id="9537e-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="9537e-130">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="9537e-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




