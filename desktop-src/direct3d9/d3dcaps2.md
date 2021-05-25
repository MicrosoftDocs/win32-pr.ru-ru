---
description: См. список флагов возможностей драйвера. Включает определения, значения и описания со ссылками на API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343379"
---
# <a name="d3dcaps2"></a><span data-ttu-id="581cd-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="581cd-104">D3DCAPS2</span></span>

<span data-ttu-id="581cd-105">Флаги возможностей драйвера.</span><span class="sxs-lookup"><span data-stu-id="581cd-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="581cd-106">#определенно</span><span class="sxs-lookup"><span data-stu-id="581cd-106">#define</span></span></td>
<td><span data-ttu-id="581cd-107">Значение</span><span class="sxs-lookup"><span data-stu-id="581cd-107">Value</span></span></td>
<td><span data-ttu-id="581cd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="581cd-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="581cd-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="581cd-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="581cd-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="581cd-110">0x40000000L</span></span></td>
<td><span data-ttu-id="581cd-111">Драйвер способен автоматически создавать MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="581cd-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="581cd-112">Дополнительные сведения см. в разделе <a href="automatic-generation-of-mipmaps.md">Автоматическое создание MIP-карты (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="581cd-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="581cd-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="581cd-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="581cd-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="581cd-114">0x00100000L</span></span></td>
<td><span data-ttu-id="581cd-115">В системе установлен калибратора, который может автоматически корректировать гамму-шкалу, чтобы результат совпадал во всех системах с калибратора.</span><span class="sxs-lookup"><span data-stu-id="581cd-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="581cd-116">Чтобы вызвать калибратора при установке новых уровней гаммы, используйте флаг D3DSGR_CALIBRATE при вызове <a href="/windows/desktop/api"><strong>сетгаммарамп</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="581cd-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="581cd-117">Калибровка гаммы увеличивает нагрузку на обработку и не должна часто использоваться.</span><span class="sxs-lookup"><span data-stu-id="581cd-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="581cd-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="581cd-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="581cd-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="581cd-119">0x80000000L</span></span></td>
<td><span data-ttu-id="581cd-120">Устройство может создавать совместно создаваемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="581cd-120">The device can create sharable resources.</span></span> <span data-ttu-id="581cd-121">Методы, создающие ресурсы, могут задавать значения, отличные от NULL, для их параметров <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>пшаредхандле</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="581cd-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="581cd-122">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="581cd-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="581cd-123">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="581cd-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="581cd-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="581cd-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="581cd-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="581cd-125">0x10000000L</span></span></td>
<td><span data-ttu-id="581cd-126">Драйвер способен управлять ресурсами.</span><span class="sxs-lookup"><span data-stu-id="581cd-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="581cd-127">Для таких драйверов D3DPOOL_MANAGED ресурсы будут управляться драйвером.</span><span class="sxs-lookup"><span data-stu-id="581cd-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="581cd-128">Чтобы Direct3D переопределял драйвер, чтобы Direct3D управлял ресурсы, используйте флаг D3DCREATE_DISABLE_DRIVER_MANAGEMENT при вызове <a href="/windows/desktop/api"><strong>креатедевице</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="581cd-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="581cd-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="581cd-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="581cd-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="581cd-130">0x20000000L</span></span></td>
<td><span data-ttu-id="581cd-131">Драйвер поддерживает динамические текстуры.</span><span class="sxs-lookup"><span data-stu-id="581cd-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="581cd-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="581cd-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="581cd-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="581cd-133">0x00020000L</span></span></td>
<td><span data-ttu-id="581cd-134">Драйвер поддерживает настройку динамической гаммы пандус в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="581cd-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="581cd-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="581cd-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="581cd-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="581cd-136">0x02000000L</span></span></td>
<td><span data-ttu-id="581cd-137">Процессу не используется.</span><span class="sxs-lookup"><span data-stu-id="581cd-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="581cd-138">Эти константы используются членом D3CAPS2 объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="581cd-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="581cd-139">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="581cd-139">Constant Information</span></span>



|  <span data-ttu-id="581cd-140">Требование</span><span class="sxs-lookup"><span data-stu-id="581cd-140">Requirement</span></span>                        | <span data-ttu-id="581cd-141">Значение</span><span class="sxs-lookup"><span data-stu-id="581cd-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="581cd-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="581cd-142">Header</span></span>                   | <span data-ttu-id="581cd-143">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="581cd-143">d3d9caps.h</span></span> |
| <span data-ttu-id="581cd-144">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="581cd-144">Minimum operating system</span></span> | <span data-ttu-id="581cd-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="581cd-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="581cd-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="581cd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="581cd-147">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="581cd-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
