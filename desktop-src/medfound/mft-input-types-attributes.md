---
description: Содержит зарегистрированные входные типы для Media Foundation преобразования (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: Атрибут MFT_INPUT_TYPES_Attributes (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543914"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="cab94-103">\_ \_ Атрибут атрибутов входных типов MFT \_</span><span class="sxs-lookup"><span data-stu-id="cab94-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="cab94-104">Содержит зарегистрированные входные типы для Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="cab94-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="cab94-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cab94-105">Data type</span></span>

<span data-ttu-id="cab94-106">**MFT \_ \_ \_ Сведения \[ о \] типе регистрации** хранятся в виде **байта \[ \]**</span><span class="sxs-lookup"><span data-stu-id="cab94-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="cab94-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="cab94-107">Get/set</span></span>

<span data-ttu-id="cab94-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="cab94-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="cab94-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="cab94-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="cab94-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cab94-110">Remarks</span></span>

<span data-ttu-id="cab94-111">Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="cab94-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="cab94-112">Этот атрибут содержит массив структур [**\_ \_ \_ сведений о типе регистра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , описывающих один или несколько форматов входных данных, поддерживаемых MFT.</span><span class="sxs-lookup"><span data-stu-id="cab94-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="cab94-113">Эти значения берутся из реестра и предназначены в качестве подсказки для приложения.</span><span class="sxs-lookup"><span data-stu-id="cab94-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="cab94-114">Таблица MFT может поддерживать дополнительные форматы.</span><span class="sxs-lookup"><span data-stu-id="cab94-114">The MFT might support additional formats.</span></span> <span data-ttu-id="cab94-115">Чтобы задать фактический формат входных данных, необходимо создать таблицу MFT и вызвать [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="cab94-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="cab94-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="cab94-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab94-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cab94-117">Requirements</span></span>



| <span data-ttu-id="cab94-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cab94-118">Requirement</span></span> | <span data-ttu-id="cab94-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cab94-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab94-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cab94-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cab94-121">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="cab94-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cab94-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cab94-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cab94-123">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="cab94-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cab94-124">Header</span><span class="sxs-lookup"><span data-stu-id="cab94-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab94-125"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="cab94-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab94-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cab94-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab94-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cab94-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cab94-128">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="cab94-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




