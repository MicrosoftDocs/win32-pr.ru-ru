---
description: Флаги возможностей драйвера.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710765"
---
# <a name="d3dcaps3"></a><span data-ttu-id="cbb1a-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="cbb1a-103">D3DCAPS3</span></span>

<span data-ttu-id="cbb1a-104">Флаги возможностей драйвера.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbb1a-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="cbb1a-105">#define</span></span></td>
<td><span data-ttu-id="cbb1a-106">Значение</span><span class="sxs-lookup"><span data-stu-id="cbb1a-106">Value</span></span></td>
<td><span data-ttu-id="cbb1a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cbb1a-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbb1a-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="cbb1a-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="cbb1a-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="cbb1a-109">0x00000020L</span></span></td>
<td><span data-ttu-id="cbb1a-110">Указывает, что устройство может учитывать состояние отображения D3DRS_ALPHABLENDENABLE в полноэкранном режиме при использовании эффектов перелистывания или отклонения.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="cbb1a-111">Это применимо только в том случае, если состояниям D3DRS_SRCBLEND или D3DRS_DESTBLEND задано одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="cbb1a-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="cbb1a-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="cbb1a-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="cbb1a-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="cbb1a-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="cbb1a-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="cbb1a-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="cbb1a-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="cbb1a-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbb1a-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="cbb1a-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="cbb1a-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="cbb1a-117">0x00000100L</span></span></td>
<td><span data-ttu-id="cbb1a-118">Устройство может ускорить копирование памяти из памяти системы в локальную видеопамять.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="cbb1a-119">Это гарантирует, что вызовы <a href="/windows/desktop/api"><strong>упдатесурфаце</strong></a> и <a href="/windows/desktop/api"><strong>упдатетекстуре</strong></a> будут аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="cbb1a-120">Если это ограничение отсутствует, эти вызовы будут выполняться, но будут выполняться медленнее.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbb1a-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="cbb1a-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="cbb1a-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="cbb1a-122">0x00000200L</span></span></td>
<td><span data-ttu-id="cbb1a-123">Устройство может ускорить копирование памяти из локальной видеопамяти в системную память.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="cbb1a-124">Это гарантирует, что вызовы <a href="/windows/desktop/api"><strong>жетрендертаржетдата</strong></a> будут аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="cbb1a-125">Если это ограничение отсутствует, вызов будет выполнен, но будет выполняться медленнее.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbb1a-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="cbb1a-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="cbb1a-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="cbb1a-127">0x00000400L</span></span></td>
<td><span data-ttu-id="cbb1a-128">Драйвер дисплея поддерживает DDI ДКСВА-HD.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="cbb1a-129">Дополнительные сведения о DDI ДКСВА-HD см. в разделе <a href="https://msdn.microsoft.com/library/dd835176.aspx">обработка High-Definition видео</a>.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbb1a-130">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="cbb1a-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="cbb1a-131">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbb1a-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="cbb1a-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="cbb1a-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="cbb1a-133">0x00000080L</span></span></td>
<td><span data-ttu-id="cbb1a-134">Указывает, что устройство может выполнять гамма-коррекцию из окна заднего буфера (с линейным содержимым) на Рабочий стол sRGB.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbb1a-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="cbb1a-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="cbb1a-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="cbb1a-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="cbb1a-137">Процессу не используется.</span><span class="sxs-lookup"><span data-stu-id="cbb1a-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cbb1a-138">Эти константы используются членом D3CAPS3 объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="cbb1a-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="cbb1a-139">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="cbb1a-139">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="cbb1a-140">Header</span><span class="sxs-lookup"><span data-stu-id="cbb1a-140">Header</span></span>                   | <span data-ttu-id="cbb1a-141">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="cbb1a-141">d3d9caps.h</span></span> |
| <span data-ttu-id="cbb1a-142">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="cbb1a-142">Minimum operating system</span></span> | <span data-ttu-id="cbb1a-143">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cbb1a-143">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cbb1a-144">См. также</span><span class="sxs-lookup"><span data-stu-id="cbb1a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb1a-145">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="cbb1a-145">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




