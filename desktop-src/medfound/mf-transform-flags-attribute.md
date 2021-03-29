---
description: Содержит флаги для объекта активации Media Foundation преобразования (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: Атрибут MF_TRANSFORM_FLAGS_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991331"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="32361-103">\_ \_ Атрибут атрибута флага MF Transform \_</span><span class="sxs-lookup"><span data-stu-id="32361-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="32361-104">Содержит флаги для объекта активации Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="32361-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="32361-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="32361-105">Data type</span></span>

<span data-ttu-id="32361-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="32361-106">**UINT32**</span></span>

<span data-ttu-id="32361-107">Значение представляет собой побитовое **или** для флагов перечисления [**\_ MFT \_ Enum \_ Flag**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) .</span><span class="sxs-lookup"><span data-stu-id="32361-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="32361-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="32361-108">Get/set</span></span>

<span data-ttu-id="32361-109">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="32361-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="32361-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="32361-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="32361-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32361-111">Remarks</span></span>

<span data-ttu-id="32361-112">Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="32361-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="32361-113">Атрибут содержит флаги, описывающие основную таблицу файлов.</span><span class="sxs-lookup"><span data-stu-id="32361-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="32361-114">Требования</span><span class="sxs-lookup"><span data-stu-id="32361-114">Requirements</span></span>



| <span data-ttu-id="32361-115">Требование</span><span class="sxs-lookup"><span data-stu-id="32361-115">Requirement</span></span> | <span data-ttu-id="32361-116">Значение</span><span class="sxs-lookup"><span data-stu-id="32361-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32361-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32361-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32361-118">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="32361-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="32361-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32361-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32361-120">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="32361-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="32361-121">Header</span><span class="sxs-lookup"><span data-stu-id="32361-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32361-122"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="32361-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32361-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32361-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32361-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32361-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32361-125">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="32361-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
