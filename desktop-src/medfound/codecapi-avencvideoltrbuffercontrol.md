---
description: Указывает максимальное число кадров длинной ссылки (LTR), управляемых приложением.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Свойство CODECAPI_AVEncVideoLTRBufferControl (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539626"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="39c8b-103">КОДЕКАПИ \_ авенквидеолтрбуфферконтрол, свойство</span><span class="sxs-lookup"><span data-stu-id="39c8b-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="39c8b-104">Указывает максимальное число кадров длинной ссылки (LTR), управляемых приложением.</span><span class="sxs-lookup"><span data-stu-id="39c8b-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="39c8b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="39c8b-105">Data type</span></span>

<span data-ttu-id="39c8b-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="39c8b-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="39c8b-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="39c8b-107">Property GUID</span></span>

<span data-ttu-id="39c8b-108">**КОДЕКАПИ \_ авенквидеолтрбуфферконтрол**</span><span class="sxs-lookup"><span data-stu-id="39c8b-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="39c8b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="39c8b-109">Property value</span></span>

<span data-ttu-id="39c8b-110">Значение этого элемента управления включает два поля, где каждое поле имеет 16 бит.</span><span class="sxs-lookup"><span data-stu-id="39c8b-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c8b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="39c8b-111">Value</span></span></th>
<th><span data-ttu-id="39c8b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="39c8b-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="39c8b-113"><dt><strong>Первое поле</strong></dt> <dt>битов [0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="39c8b-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="39c8b-114">Число кадров LTR, управляемых приложением.</span><span class="sxs-lookup"><span data-stu-id="39c8b-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="39c8b-115"><strong>Кодировщики H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="39c8b-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="39c8b-116">Предполагая, что значение N, а N — ненулевое значение, в каждом кадре IDR кодировщик должен автоматически пометить кадры, следующие за кадром IDR (включая фрейм IDR), как кадры LTR, если все три из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="39c8b-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="39c8b-117">Рамка еще не помечена как рамка долгосрочной ссылки.</span><span class="sxs-lookup"><span data-stu-id="39c8b-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="39c8b-118">Кадр является основным кадром слоя.</span><span class="sxs-lookup"><span data-stu-id="39c8b-118">The frame is a base layer frame.</span></span> <span data-ttu-id="39c8b-119">Например, элемент синтаксиса <strong>temporal_id</strong> равен 0.</span><span class="sxs-lookup"><span data-stu-id="39c8b-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="39c8b-120">Число кадров, помеченных в настоящий момент как LTR, меньше N.</span><span class="sxs-lookup"><span data-stu-id="39c8b-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="39c8b-121"><dt><strong>Второе поле</strong></dt> <dt>битов [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="39c8b-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="39c8b-122">Режим доверия для элемента управления LTR.</span><span class="sxs-lookup"><span data-stu-id="39c8b-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="39c8b-123"><strong>Кодировщики H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="39c8b-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="39c8b-124">1 (отношение доверия до) означает, что кодировщик может использовать рамку LTR, если только приложение явно не сделает его через элемент управления <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> .</span><span class="sxs-lookup"><span data-stu-id="39c8b-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="39c8b-125">Другие значения являются недопустимыми и зарезервированы для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="39c8b-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="39c8b-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39c8b-126">Remarks</span></span>

<span data-ttu-id="39c8b-127">Это статический API.</span><span class="sxs-lookup"><span data-stu-id="39c8b-127">This is a static API.</span></span>

<span data-ttu-id="39c8b-128">Значение по умолчанию должно быть равно 0</span><span class="sxs-lookup"><span data-stu-id="39c8b-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="39c8b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="39c8b-129">Requirements</span></span>



| <span data-ttu-id="39c8b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="39c8b-130">Requirement</span></span> | <span data-ttu-id="39c8b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="39c8b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39c8b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39c8b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39c8b-133">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="39c8b-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="39c8b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39c8b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39c8b-135">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="39c8b-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="39c8b-136">Header</span><span class="sxs-lookup"><span data-stu-id="39c8b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c8b-137"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c8b-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c8b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39c8b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c8b-139">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39c8b-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




