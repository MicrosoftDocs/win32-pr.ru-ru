---
description: Представляет сведения о конкретном.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пикселхисторинтерсектион
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701153"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="f8bff-103"><span id="vspixengine.pixelhistoryintersection"></span>Структура Пикселхисторинтерсектион</span><span class="sxs-lookup"><span data-stu-id="f8bff-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="f8bff-104">Представляет сведения об определенном</span><span class="sxs-lookup"><span data-stu-id="f8bff-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8bff-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="f8bff-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f8bff-106">Members</span></span>

<span data-ttu-id="f8bff-107">**фраменумбер**</span><span class="sxs-lookup"><span data-stu-id="f8bff-107">**frameNumber**</span></span>  
<span data-ttu-id="f8bff-108">Кадр графического события, связана с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f8bff-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="f8bff-109">**Аль**</span><span class="sxs-lookup"><span data-stu-id="f8bff-109">**eid**</span></span>  
<span data-ttu-id="f8bff-110">Идентификатор события графики, связанного с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f8bff-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="f8bff-111">**рендертаржетптр**</span><span class="sxs-lookup"><span data-stu-id="f8bff-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="f8bff-112">Целевой объект прорисовки, изначально связанный (внутри захваченного приложения) с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f8bff-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="f8bff-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="f8bff-113">**eventType**</span></span>  
<span data-ttu-id="f8bff-114">Тип события, связанного с этой операцией (в частности, является ли это событие вызовом Draw).</span><span class="sxs-lookup"><span data-stu-id="f8bff-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="f8bff-115">**точки**</span><span class="sxs-lookup"><span data-stu-id="f8bff-115">**point**</span></span>  
<span data-ttu-id="f8bff-116">Координаты пикселя в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="f8bff-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="f8bff-117">**бассемблерстажеженератесинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="f8bff-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="f8bff-118">значение true, если входной ассемблер создает идентификаторы экземпляров; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="f8bff-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="f8bff-119">**flags**</span><span class="sxs-lookup"><span data-stu-id="f8bff-119">**flags**</span></span>  
<span data-ttu-id="f8bff-120">Сочетание значений ПИКСЕЛХИСТОРИФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="f8bff-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="f8bff-121">Дополнительные сведения см. в описании перечисления ПИКСЕЛХИСТОРИФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="f8bff-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="f8bff-122">**фбинитиалред**</span><span class="sxs-lookup"><span data-stu-id="f8bff-122">**fbInitialRed**</span></span>  
<span data-ttu-id="f8bff-123">Буфера кадров: значение красного цвета компонента буфера кадров перед слиянием выходных данных шейдера пикселей; то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-124">**фбинитиалгрин**</span><span class="sxs-lookup"><span data-stu-id="f8bff-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="f8bff-125">Буфера кадров: значение зеленого компонента цвета буфера кадров перед слиянием выходных данных шейдера пикселей; то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-126">**фбинитиалблуе**</span><span class="sxs-lookup"><span data-stu-id="f8bff-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="f8bff-127">Буфера кадров: значение синего компонента цвета буфера кадров перед слиянием выходных данных шейдера пикселей; то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-128">**фбинитиалалфа**</span><span class="sxs-lookup"><span data-stu-id="f8bff-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="f8bff-129">Буфера кадров: значение альфа-компонента цвета буфера кадров перед слиянием выходных данных шейдера пикселей; то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-130">**лабелфбинитиалред**</span><span class="sxs-lookup"><span data-stu-id="f8bff-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="f8bff-131">Строка COM, содержащая имя метки, связанной с компонентом красного цвета буфера кадров перед заливкой пикселей. то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-132">**лабелфбинитиалгрин**</span><span class="sxs-lookup"><span data-stu-id="f8bff-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="f8bff-133">Строка COM, содержащая имя метки, связанной с компонентом зеленого цвета буфера кадров перед заливкой пикселей. то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-134">**лабелфбинитиалблуе**</span><span class="sxs-lookup"><span data-stu-id="f8bff-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="f8bff-135">Строка COM, содержащая имя метки, связанной с компонентом синего цвета буфера кадров перед заливкой пикселей. то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-136">**лабелфбинитиалалфа**</span><span class="sxs-lookup"><span data-stu-id="f8bff-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="f8bff-137">Строка COM, содержащая имя метки, связанной с компонентом цвета альфа буфера кадров, перед заливкой пикселей. то есть в начале этого кадра.</span><span class="sxs-lookup"><span data-stu-id="f8bff-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="f8bff-138">**фбред**</span><span class="sxs-lookup"><span data-stu-id="f8bff-138">**fbRed**</span></span>  
<span data-ttu-id="f8bff-139">Буфера кадров: значение красного цвета компонента буфера кадров после слияния всех выходных данных шейдера пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-140">**фбгрин**</span><span class="sxs-lookup"><span data-stu-id="f8bff-140">**fbGreen**</span></span>  
<span data-ttu-id="f8bff-141">Буфера кадров: значение зеленого компонента цвета буфера кадров после слияния всех выходных данных шейдера пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-142">**фбблуе**</span><span class="sxs-lookup"><span data-stu-id="f8bff-142">**fbBlue**</span></span>  
<span data-ttu-id="f8bff-143">Буфера кадров: значение синего компонента цвета буфера кадров после слияния всех выходных данных шейдера пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-144">**фбалфа**</span><span class="sxs-lookup"><span data-stu-id="f8bff-144">**fbAlpha**</span></span>  
<span data-ttu-id="f8bff-145">Буфера кадров: значение альфа-компонента цвета буфера кадров после слияния всех выходных данных шейдера пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-146">**лабелфбред**</span><span class="sxs-lookup"><span data-stu-id="f8bff-146">**LabelFBRed**</span></span>  
<span data-ttu-id="f8bff-147">Строка COM, содержащая имя метки, связанной с компонентом красного цвета буфера кадров после всей заливки пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-148">**лабелфбгрин**</span><span class="sxs-lookup"><span data-stu-id="f8bff-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="f8bff-149">Строка COM, содержащая имя метки, связанной с компонентом зеленого цвета буфера кадров после всей заливки пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-150">**лабелфбблуе**</span><span class="sxs-lookup"><span data-stu-id="f8bff-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="f8bff-151">Строка COM, содержащая имя метки, связанной с компонентом синего цвета буфера кадров после заливки пикселя. то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-152">**лабелфбалфа**</span><span class="sxs-lookup"><span data-stu-id="f8bff-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="f8bff-153">Строка COM, содержащая имя метки, связанной с компонентом цвета альфа-составляющей буфера кадров после всей заливки пикселей; то есть окончательный буфера кадров цвет.</span><span class="sxs-lookup"><span data-stu-id="f8bff-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="f8bff-154">**пикселкиллреасон**</span><span class="sxs-lookup"><span data-stu-id="f8bff-154">**pixelKillReason**</span></span>  
<span data-ttu-id="f8bff-155">Указывает причину, по которой был уничтожен цветовой вклад пикселя.</span><span class="sxs-lookup"><span data-stu-id="f8bff-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="f8bff-156">**Состав**</span><span class="sxs-lookup"><span data-stu-id="f8bff-156">**HResult**</span></span>  
<span data-ttu-id="f8bff-157">При возникновении ошибки содержит значение HRESULT, которое указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="f8bff-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8bff-158">Требования</span><span class="sxs-lookup"><span data-stu-id="f8bff-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f8bff-159">Header</span><span class="sxs-lookup"><span data-stu-id="f8bff-159">Header</span></span></p></td><td><span data-ttu-id="f8bff-160">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f8bff-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



