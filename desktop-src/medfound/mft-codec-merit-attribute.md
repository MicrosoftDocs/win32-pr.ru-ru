---
description: Содержит значение неустановленного аппаратного кодека.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Атрибут MFT_CODEC_MERIT_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656556"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="61b0c-103">\_ \_ Атрибут атрибута «неуспешный кодек MFT» \_</span><span class="sxs-lookup"><span data-stu-id="61b0c-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="61b0c-104">Содержит значение неустановленного аппаратного кодека.</span><span class="sxs-lookup"><span data-stu-id="61b0c-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="61b0c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="61b0c-105">Data type</span></span>

<span data-ttu-id="61b0c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="61b0c-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="61b0c-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="61b0c-107">Get/set</span></span>

<span data-ttu-id="61b0c-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="61b0c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="61b0c-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="61b0c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="61b0c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61b0c-110">Remarks</span></span>

<span data-ttu-id="61b0c-111">Этот атрибут задается в объекте активации для Media Foundation преобразования (MFT), представляющего аппаратный кодек.</span><span class="sxs-lookup"><span data-stu-id="61b0c-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="61b0c-112">Значением атрибута является значение «неуспешный» кодека.</span><span class="sxs-lookup"><span data-stu-id="61b0c-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="61b0c-113">Этот атрибут управляет порядком, в котором функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) перечисляет кодеки, если установлен флаг **\_ \_ \_ сортандфилтер флага перечисления MFT** .</span><span class="sxs-lookup"><span data-stu-id="61b0c-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="61b0c-114">МФТС со значением в списке выше, чем у других МФТС.</span><span class="sxs-lookup"><span data-stu-id="61b0c-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="61b0c-115">Этот атрибут не содержит надежного значения.</span><span class="sxs-lookup"><span data-stu-id="61b0c-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="61b0c-116">Чтобы проверить фактическое значение соответствия кодека, вызовите функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="61b0c-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="61b0c-117">Если значение \_ \_ атрибута атрибута «несоответствие кодека MFT \_ » не совпадает со значением, полученным с помощью [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), метод [**имфактивате:: Активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) завершается сбоем и возвращает **MF \_ E \_ Недопустимый \_ кодек \_**.</span><span class="sxs-lookup"><span data-stu-id="61b0c-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="61b0c-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="61b0c-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b0c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="61b0c-119">Requirements</span></span>



| <span data-ttu-id="61b0c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="61b0c-120">Requirement</span></span> | <span data-ttu-id="61b0c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="61b0c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b0c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61b0c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61b0c-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="61b0c-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="61b0c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61b0c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61b0c-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="61b0c-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="61b0c-126">Header</span><span class="sxs-lookup"><span data-stu-id="61b0c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b0c-127"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b0c-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b0c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61b0c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b0c-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61b0c-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="61b0c-130">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="61b0c-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




