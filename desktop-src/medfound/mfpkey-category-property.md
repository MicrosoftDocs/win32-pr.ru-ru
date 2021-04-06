---
description: Содержит GUID категории для Media Foundation преобразования (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Свойство MFPKEY_CATEGORY (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910195"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="4db54-103">МФПКЭЙ, \_ свойство категории</span><span class="sxs-lookup"><span data-stu-id="4db54-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="4db54-104">Содержит GUID категории для Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="4db54-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="4db54-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4db54-105">Data type</span></span>

<span data-ttu-id="4db54-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="4db54-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4db54-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="4db54-107">PROPVARIANT member</span></span>

<span data-ttu-id="4db54-108">**GUID** (**CLSID** \* )</span><span class="sxs-lookup"><span data-stu-id="4db54-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="4db54-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="4db54-109">VT\_CLSID</span></span>

<span data-ttu-id="4db54-110">**пууид**</span><span class="sxs-lookup"><span data-stu-id="4db54-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="4db54-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4db54-111">Remarks</span></span>

<span data-ttu-id="4db54-112">Значением этого свойства является идентификатор GUID, определяющий категорию MFT.</span><span class="sxs-lookup"><span data-stu-id="4db54-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="4db54-113">Список категорий см. в разделе [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="4db54-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="4db54-114">Это свойство является необязательным и является информационным.</span><span class="sxs-lookup"><span data-stu-id="4db54-114">This property is optional and is informational only.</span></span> <span data-ttu-id="4db54-115">Таблица MFT может использовать это свойство для сообщения категории, под которой он зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="4db54-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="4db54-116">Чтобы получить это свойство, запросите MFT для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="4db54-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="4db54-117">Чтобы перечислить категорию MFT, вызовите функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="4db54-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="4db54-118">Нет прямой связи между функцией **мфтенум** и этим свойством.</span><span class="sxs-lookup"><span data-stu-id="4db54-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db54-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4db54-119">Requirements</span></span>



| <span data-ttu-id="4db54-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4db54-120">Requirement</span></span> | <span data-ttu-id="4db54-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4db54-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db54-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4db54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4db54-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4db54-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4db54-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4db54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4db54-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4db54-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4db54-126">Header</span><span class="sxs-lookup"><span data-stu-id="4db54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4db54-127"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="4db54-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db54-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db54-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db54-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4db54-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4db54-130">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4db54-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




