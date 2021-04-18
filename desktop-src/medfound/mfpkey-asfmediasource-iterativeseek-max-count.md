---
description: Задает максимальное число итераций поиска, которые будут использоваться источником ASF Media при выполнении итеративного поиска.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: Свойство MFPKEY_ASFMediaSource_IterativeSeek_Max_Count (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693876"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="633bd-103">МФПКЭЙ \_ асфмедиасаурце \_ итеративесик \_ Max \_ Count, свойство</span><span class="sxs-lookup"><span data-stu-id="633bd-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="633bd-104">Задает максимальное число итераций поиска, которые будут использоваться источником ASF Media при выполнении итеративного поиска.</span><span class="sxs-lookup"><span data-stu-id="633bd-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="633bd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="633bd-105">Data type</span></span>

<span data-ttu-id="633bd-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="633bd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="633bd-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="633bd-107">PROPVARIANT member</span></span>

<span data-ttu-id="633bd-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="633bd-108">**ULONG**</span></span>

<span data-ttu-id="633bd-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="633bd-109">VT\_UI4</span></span>

<span data-ttu-id="633bd-110">**улвал**</span><span class="sxs-lookup"><span data-stu-id="633bd-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="633bd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="633bd-111">Remarks</span></span>

<span data-ttu-id="633bd-112">Это свойство используется для настройки источника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="633bd-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="633bd-113">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="633bd-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="633bd-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="633bd-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="633bd-115">Это свойство применяется, только если включено итеративное Поиск.</span><span class="sxs-lookup"><span data-stu-id="633bd-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="633bd-116">Дополнительные сведения см. в разделе [мфпкэй \_ асфмедиасаурце \_ итеративесикифноиндекс](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="633bd-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="633bd-117">Допустимый диапазон этого свойства — \[ 1-10 \] включительно.</span><span class="sxs-lookup"><span data-stu-id="633bd-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="633bd-118">С большим числом итеративное Поиск, как правило, будет более точным, но занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="633bd-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="633bd-119">Значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="633bd-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="633bd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="633bd-120">Requirements</span></span>



| <span data-ttu-id="633bd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="633bd-121">Requirement</span></span> | <span data-ttu-id="633bd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="633bd-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="633bd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="633bd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="633bd-124">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="633bd-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="633bd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="633bd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="633bd-126">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="633bd-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="633bd-127">Header</span><span class="sxs-lookup"><span data-stu-id="633bd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="633bd-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="633bd-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633bd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="633bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633bd-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="633bd-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




