---
title: ЕКУАЛИЗЕРСЕТТИНГС. плавный переход
description: Атрибут «плавный переход» указывает или получает значение, указывающее, включен ли перекрестное выцветание.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- ЕКУАЛИЗЕРСЕТТИНГС. плавный переход проигрывателя Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699168"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="1a34e-104">ЕКУАЛИЗЕРСЕТТИНГС. плавный переход</span><span class="sxs-lookup"><span data-stu-id="1a34e-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="1a34e-105">Атрибут « **плавный** переход» указывает или получает значение, указывающее, включен ли перекрестное выцветание.</span><span class="sxs-lookup"><span data-stu-id="1a34e-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="1a34e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1a34e-106">Possible Values</span></span>

<span data-ttu-id="1a34e-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1a34e-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1a34e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1a34e-108">Value</span></span> | <span data-ttu-id="1a34e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1a34e-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="1a34e-110">true</span><span class="sxs-lookup"><span data-stu-id="1a34e-110">true</span></span>  | <span data-ttu-id="1a34e-111">Перекрестное выцветание включено.</span><span class="sxs-lookup"><span data-stu-id="1a34e-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="1a34e-112">false</span><span class="sxs-lookup"><span data-stu-id="1a34e-112">false</span></span> | <span data-ttu-id="1a34e-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a34e-113">Default.</span></span> <span data-ttu-id="1a34e-114">Перекрестное выцветание отключено.</span><span class="sxs-lookup"><span data-stu-id="1a34e-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1a34e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a34e-115">Remarks</span></span>

<span data-ttu-id="1a34e-116">Перекрестное выцветание — это функция обработки звука, которая постепенно уменьшает объем одного элемента мультимедиа рядом с концом его воспроизведения, одновременно запуская воспроизведение следующего элемента мультимедиа на минимальном Томе и постепенно увеличивая его до обычного тома.</span><span class="sxs-lookup"><span data-stu-id="1a34e-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="1a34e-117">Перекрытие между началом второго элемента мультимедиа и концом первого элемента мультимедиа задается атрибутом **кроссфадевиндов** .</span><span class="sxs-lookup"><span data-stu-id="1a34e-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a34e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1a34e-118">Requirements</span></span>



| <span data-ttu-id="1a34e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1a34e-119">Requirement</span></span> | <span data-ttu-id="1a34e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1a34e-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1a34e-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1a34e-121">Version</span></span><br/> | <span data-ttu-id="1a34e-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1a34e-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a34e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a34e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a34e-124">**ЕКУАЛИЗЕРСЕТТИНГС, элемент**</span><span class="sxs-lookup"><span data-stu-id="1a34e-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="1a34e-125">**ЕКУАЛИЗЕРСЕТТИНГС. Кроссфадевиндов**</span><span class="sxs-lookup"><span data-stu-id="1a34e-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





