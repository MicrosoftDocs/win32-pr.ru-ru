---
description: Указывает, использует ли источник мультимедиа ASF приближенное Поиск.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Свойство MFPKEY_ASFMediaSource_ApproxSeek (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693878"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="a4f5d-103">МФПКЭЙ \_ асфмедиасаурце \_ аппрокссик, свойство</span><span class="sxs-lookup"><span data-stu-id="a4f5d-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="a4f5d-104">Указывает, использует ли источник мультимедиа ASF приближенное Поиск.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="a4f5d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a4f5d-105">Data type</span></span>

<span data-ttu-id="a4f5d-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="a4f5d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a4f5d-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="a4f5d-107">PROPVARIANT member</span></span>

<span data-ttu-id="a4f5d-108">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a4f5d-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="a4f5d-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="a4f5d-109">VT\_BOOL</span></span>

<span data-ttu-id="a4f5d-110">**булвал**</span><span class="sxs-lookup"><span data-stu-id="a4f5d-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a4f5d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4f5d-111">Remarks</span></span>

<span data-ttu-id="a4f5d-112">Приложения могут использовать это свойство для настройки источника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="a4f5d-113">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a4f5d-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a4f5d-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="a4f5d-115">Источник мультимедиа ASF обрабатывает Поиск следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a4f5d-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="a4f5d-116">Если значение этого свойства равно **\_ true**, источник мультимедиа использует приблизительное Поиск, что менее точное, но быстрее, чем точное Поиск.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="a4f5d-117">Если значение является **вариантным \_ false** , а ASF-файл имеет индекс, источник мультимедиа использует точное Поиск.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="a4f5d-118">Если файл ASF не содержит индекс, источник мультимедиа использует поиск аппроксмате, если свойство [мфпкэй \_ асфмедиасаурце \_ итеративесикифноиндекс](mfpkey-asfmediasource-iterativeseekifnoindex.md) не имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="a4f5d-119">Если ASF-файл не содержит индекс, а свойство [мфпкэй \_ асфмедиасаурце \_ Итеративесикифноиндекс](mfpkey-asfmediasource-iterativeseekifnoindex.md) имеет значение **Variant \_ true**, источник мультимедиа использует итеративное Поиск.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="a4f5d-120">Итеративное Поиск является более точным, но медленнее, чем приближенное (но обычно менее точное, чем точное Поиск).</span><span class="sxs-lookup"><span data-stu-id="a4f5d-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="a4f5d-121">Требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="a4f5d-122">Значение этого свойства по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a4f5d-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f5d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a4f5d-123">Requirements</span></span>



| <span data-ttu-id="a4f5d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a4f5d-124">Requirement</span></span> | <span data-ttu-id="a4f5d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a4f5d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f5d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4f5d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f5d-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4f5d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a4f5d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4f5d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f5d-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4f5d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a4f5d-130">Header</span><span class="sxs-lookup"><span data-stu-id="a4f5d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f5d-131"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f5d-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f5d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4f5d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f5d-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4f5d-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




