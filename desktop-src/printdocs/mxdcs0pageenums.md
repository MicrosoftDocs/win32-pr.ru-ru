---
description: Перечисление перечислений \_ страниц мксдк S0 \_ \_ используется для указания типов ресурсов, которые могут быть связаны со страницами в документах XPS и могут обрабатываться или передаваться необработанным конвертером документов XPS (мксдк) в выходные данные.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Перечисление MXDC_S0_PAGE_ENUMS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909576"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="e7257-103">Перечисление перечислений \_ страниц мксдк S0 \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7257-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="e7257-104">Перечисление перечислений **\_ \_ страниц \_ мксдк S0** используется для указания типов ресурсов, которые могут быть связаны со страницами в документах XPS и могут обрабатываться или передаваться необработанным конвертером документов XPS (мксдк) в выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e7257-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7257-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7257-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="e7257-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e7257-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e7257-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**МКСДК \_ Resource \_ TTF**</span><span class="sxs-lookup"><span data-stu-id="e7257-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-108">Шрифт TrueType или OpenType.</span><span class="sxs-lookup"><span data-stu-id="e7257-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**МКСДК \_ ресурс \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="e7257-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-110">Изображение JPEG</span><span class="sxs-lookup"><span data-stu-id="e7257-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="e7257-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**МКСДК \_ ресурс \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="e7257-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-112">Изображение PNG.</span><span class="sxs-lookup"><span data-stu-id="e7257-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**МКСДК \_ ресурсов \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="e7257-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-114">Изображение TIFF.</span><span class="sxs-lookup"><span data-stu-id="e7257-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**\_формате WDP ресурсов \_ мксдк**</span><span class="sxs-lookup"><span data-stu-id="e7257-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-116">Изображение Windows Media Photo.</span><span class="sxs-lookup"><span data-stu-id="e7257-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_словарь ресурсов \_ мксдк**</span><span class="sxs-lookup"><span data-stu-id="e7257-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-118">Удаленный словарь ресурсов, который должен быть передан в выходные данные МКСДК, не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="e7257-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ профиль ICC ресурса \_ мксдк**</span><span class="sxs-lookup"><span data-stu-id="e7257-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-120">Профиль ICC, который должен быть передан в выходные данные МКСДК, не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="e7257-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_ \_ эскиз JPEG ресурса \_ мксдк**</span><span class="sxs-lookup"><span data-stu-id="e7257-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-122">Эскиз JPEG, который должен быть передан в выходные данные МКСДК в необработанном виде.</span><span class="sxs-lookup"><span data-stu-id="e7257-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_эскиз ресурса \_ PNG \_ мксдк**</span><span class="sxs-lookup"><span data-stu-id="e7257-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-124">Эскиз PNG, который должен быть передан в выходные данные МКСДК в необработанном виде.</span><span class="sxs-lookup"><span data-stu-id="e7257-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="e7257-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**\_ \_ максимальный размер ресурса мксдк**</span><span class="sxs-lookup"><span data-stu-id="e7257-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="e7257-126">Максимальное число ресурсов для проверки.</span><span class="sxs-lookup"><span data-stu-id="e7257-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7257-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7257-127">Remarks</span></span>

<span data-ttu-id="e7257-128">Это перечисление в основном используется в качестве члена **двресаурцетипе** структуры [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="e7257-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7257-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e7257-129">Requirements</span></span>



| <span data-ttu-id="e7257-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e7257-130">Requirement</span></span> | <span data-ttu-id="e7257-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e7257-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7257-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7257-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e7257-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7257-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e7257-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7257-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e7257-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7257-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e7257-136">Header</span><span class="sxs-lookup"><span data-stu-id="e7257-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7257-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7257-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




