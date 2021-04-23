---
description: Представляет сведения о журнале пикселей.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пикселхисторйоператион
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701125"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="2e53c-103"><span id="vspixengine.pixelhistoryoperation"></span>Структура Пикселхисторйоператион</span><span class="sxs-lookup"><span data-stu-id="2e53c-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="2e53c-104">Представляет сведения о журнале пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e53c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e53c-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="2e53c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="2e53c-106">Members</span></span>

<span data-ttu-id="2e53c-107">**Аль**</span><span class="sxs-lookup"><span data-stu-id="2e53c-107">**eid**</span></span>  
<span data-ttu-id="2e53c-108">Идентификатор события графики, связанного с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="2e53c-109">**PCP**</span><span class="sxs-lookup"><span data-stu-id="2e53c-109">**PCP**</span></span>  
<span data-ttu-id="2e53c-110">Упакованные вызовы, связанные с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="2e53c-111">**рендертаржетптр**</span><span class="sxs-lookup"><span data-stu-id="2e53c-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="2e53c-112">Целевой объект прорисовки, изначально связанный (внутри захваченного приложения) с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="2e53c-113">**иприм**</span><span class="sxs-lookup"><span data-stu-id="2e53c-113">**iPrim**</span></span>  
<span data-ttu-id="2e53c-114">Индекс фактического примитива, связанного с его операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="2e53c-115">**нумпримс**</span><span class="sxs-lookup"><span data-stu-id="2e53c-115">**numPrims**</span></span>  
<span data-ttu-id="2e53c-116">Общее число примитивов, связанных с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="2e53c-117">**нумвертсперприм**</span><span class="sxs-lookup"><span data-stu-id="2e53c-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="2e53c-118">Количество вершин на примитив.</span><span class="sxs-lookup"><span data-stu-id="2e53c-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="2e53c-119">**иинстанце**</span><span class="sxs-lookup"><span data-stu-id="2e53c-119">**iInstance**</span></span>  
<span data-ttu-id="2e53c-120">При отрисовке экземпляров — номер экземпляра фактического экземпляра, связанного с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="2e53c-121">**иинстанцекаунт**</span><span class="sxs-lookup"><span data-stu-id="2e53c-121">**iInstanceCount**</span></span>  
<span data-ttu-id="2e53c-122">При отрисовке экземпляров — общее количество экземпляров, связанных с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="2e53c-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="2e53c-123">**бассемблерстажеженератесинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="2e53c-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="2e53c-124">значение true, если входной ассемблер создает идентификаторы экземпляров; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="2e53c-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="2e53c-125">**flags**</span><span class="sxs-lookup"><span data-stu-id="2e53c-125">**flags**</span></span>  
<span data-ttu-id="2e53c-126">Сочетание значений ПИКСЕЛХИСТОРИФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="2e53c-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="2e53c-127">Дополнительные сведения см. в описании перечисления ПИКСЕЛХИСТОРИФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="2e53c-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="2e53c-128">**пвсфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-128">**pVSFile**</span></span>  
<span data-ttu-id="2e53c-129">ФИЛЕПТР для потока байтов построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="2e53c-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="2e53c-130">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="2e53c-131">**пгсфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-131">**pGSFile**</span></span>  
<span data-ttu-id="2e53c-132">ФИЛЕПТР для потока байтов шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="2e53c-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="2e53c-133">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="2e53c-134">**ппсфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-134">**pPSFile**</span></span>  
<span data-ttu-id="2e53c-135">ФИЛЕПТР для потока байтов построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="2e53c-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="2e53c-136">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="2e53c-137">**фсфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-137">**pHSFile**</span></span>  
<span data-ttu-id="2e53c-138">ФИЛЕПТР для потока байтов шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="2e53c-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="2e53c-139">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="2e53c-140">**пдсфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-140">**pDSFile**</span></span>  
<span data-ttu-id="2e53c-141">ФИЛЕПТР для потока байтов шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="2e53c-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="2e53c-142">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="2e53c-143">**пксфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-143">**pCSFile**</span></span>  
<span data-ttu-id="2e53c-144">ФИЛЕПТР для потока байтов вычислений COMPUTE Shader.</span><span class="sxs-lookup"><span data-stu-id="2e53c-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="2e53c-145">Это значение передается обратно для отладки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="2e53c-146">**вертексшадерфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="2e53c-147">Строка COM, содержащая путь к файлу исходного файла шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="2e53c-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="2e53c-148">**пикселшадерфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="2e53c-149">Строка COM, содержащая путь к файлу исходного кода шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="2e53c-150">**жеометришадерфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="2e53c-151">Строка COM, содержащая путь к файлу файла исходного шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="2e53c-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="2e53c-152">**хуллшадерфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-152">**HullShaderFile**</span></span>  
<span data-ttu-id="2e53c-153">Строка COM, содержащая путь к файлу исходного файла шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="2e53c-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="2e53c-154">**домаиншадерфиле**</span><span class="sxs-lookup"><span data-stu-id="2e53c-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="2e53c-155">Строка COM, содержащая путь к файлу исходного файла шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="2e53c-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="2e53c-156">**псред**</span><span class="sxs-lookup"><span data-stu-id="2e53c-156">**psRed**</span></span>  
<span data-ttu-id="2e53c-157">Выходные данные шейдера пикселей: значение красного цвета компонента.</span><span class="sxs-lookup"><span data-stu-id="2e53c-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="2e53c-158">**псгрин**</span><span class="sxs-lookup"><span data-stu-id="2e53c-158">**psGreen**</span></span>  
<span data-ttu-id="2e53c-159">Выходные данные шейдера пикселей: значение зеленого компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="2e53c-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="2e53c-160">**псблуе**</span><span class="sxs-lookup"><span data-stu-id="2e53c-160">**psBlue**</span></span>  
<span data-ttu-id="2e53c-161">Выходные данные шейдера пикселей: значение синего компонента цвета</span><span class="sxs-lookup"><span data-stu-id="2e53c-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="2e53c-162">**псалфа**</span><span class="sxs-lookup"><span data-stu-id="2e53c-162">**psAlpha**</span></span>  
<span data-ttu-id="2e53c-163">Выходные данные шейдера пикселей: значение компонента цвета Alpha</span><span class="sxs-lookup"><span data-stu-id="2e53c-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="2e53c-164">**лабелпсред**</span><span class="sxs-lookup"><span data-stu-id="2e53c-164">**LabelPSRed**</span></span>  
<span data-ttu-id="2e53c-165">Строка COM, содержащая имя метки, связанной с компонентом красного цвета в выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="2e53c-166">**лабелпсгрин**</span><span class="sxs-lookup"><span data-stu-id="2e53c-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="2e53c-167">Строка COM, содержащая имя метки, связанной с компонентом зеленого цвета в выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="2e53c-168">**лабелпсблуе**</span><span class="sxs-lookup"><span data-stu-id="2e53c-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="2e53c-169">Строка COM, содержащая имя метки, связанной с компонентом синего цвета выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="2e53c-170">**лабелпсалфа**</span><span class="sxs-lookup"><span data-stu-id="2e53c-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="2e53c-171">Строка COM, содержащая имя метки, связанной с компонентом цвета альфа-канала выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="2e53c-172">**пикселкиллреасон**</span><span class="sxs-lookup"><span data-stu-id="2e53c-172">**pixelKillReason**</span></span>  
<span data-ttu-id="2e53c-173">Выходные данные шейдера пикселей: Причина завершения вывода пикселя.</span><span class="sxs-lookup"><span data-stu-id="2e53c-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="2e53c-174">**пикселокклудед**</span><span class="sxs-lookup"><span data-stu-id="2e53c-174">**pixelOccluded**</span></span>  
<span data-ttu-id="2e53c-175">true, если пиксель имеет значение перекрыто; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="2e53c-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="2e53c-176">**фбред**</span><span class="sxs-lookup"><span data-stu-id="2e53c-176">**fbRed**</span></span>  
<span data-ttu-id="2e53c-177">Буфера кадров: значение красного цвета компонента буфера кадров перед слиянием выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2e53c-178">**фбгрин**</span><span class="sxs-lookup"><span data-stu-id="2e53c-178">**fbGreen**</span></span>  
<span data-ttu-id="2e53c-179">Буфера кадров: значение зеленого компонента цвета буфера кадров перед слиянием выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2e53c-180">**фбблуе**</span><span class="sxs-lookup"><span data-stu-id="2e53c-180">**fbBlue**</span></span>  
<span data-ttu-id="2e53c-181">Буфера кадров: значение синего компонента цвета буфера кадров перед слиянием выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2e53c-182">**фбалфа**</span><span class="sxs-lookup"><span data-stu-id="2e53c-182">**fbAlpha**</span></span>  
<span data-ttu-id="2e53c-183">Буфера кадров: значение альфа-компонента цвета буфера кадров перед слиянием выходных данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e53c-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2e53c-184">**лабелфбред**</span><span class="sxs-lookup"><span data-stu-id="2e53c-184">**LabelFBRed**</span></span>  
<span data-ttu-id="2e53c-185">Строка COM, содержащая имя метки, связанной с компонентом красного цвета буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2e53c-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="2e53c-186">**лабелфбгрин**</span><span class="sxs-lookup"><span data-stu-id="2e53c-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="2e53c-187">Строка COM, содержащая имя метки, связанной с компонентом зеленого цвета буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2e53c-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="2e53c-188">**лабелфбблуе**</span><span class="sxs-lookup"><span data-stu-id="2e53c-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="2e53c-189">Строка COM, содержащая имя метки, связанной с компонентом синего цвета буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2e53c-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="2e53c-190">**лабелфбалфа**</span><span class="sxs-lookup"><span data-stu-id="2e53c-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="2e53c-191">Строка COM, содержащая имя метки, связанной с компонентом цвета альфа-канала буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2e53c-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="2e53c-192">**Topology**</span><span class="sxs-lookup"><span data-stu-id="2e53c-192">**topology**</span></span>  
<span data-ttu-id="2e53c-193">Топология вершин вызовов Draw (список треугольников, полоска треугольника и т. д.).</span><span class="sxs-lookup"><span data-stu-id="2e53c-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="2e53c-194">**вершины**</span><span class="sxs-lookup"><span data-stu-id="2e53c-194">**vertices**</span></span>  
<span data-ttu-id="2e53c-195">Строка COM, содержащая буфер вершин, начиная с этого примитива.</span><span class="sxs-lookup"><span data-stu-id="2e53c-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="2e53c-196">Буфер вершин соответствует формату входного макета, указанному на этапе конвейера.</span><span class="sxs-lookup"><span data-stu-id="2e53c-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="2e53c-197">**вертекссизе**</span><span class="sxs-lookup"><span data-stu-id="2e53c-197">**vertexSize**</span></span>  
<span data-ttu-id="2e53c-198">Размер одной вершины в байтах.</span><span class="sxs-lookup"><span data-stu-id="2e53c-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="2e53c-199">**инпутлайаут**</span><span class="sxs-lookup"><span data-stu-id="2e53c-199">**InputLayout**</span></span>  
<span data-ttu-id="2e53c-200">Строка COM, содержащая последовательность структур Инпутлайаутструкт, связанных с вызовом Draw.</span><span class="sxs-lookup"><span data-stu-id="2e53c-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="2e53c-201">**Состав**</span><span class="sxs-lookup"><span data-stu-id="2e53c-201">**HResult**</span></span>  
<span data-ttu-id="2e53c-202">Значение HRESULT для DirectX.</span><span class="sxs-lookup"><span data-stu-id="2e53c-202">The DirectX Hresult.</span></span> <span data-ttu-id="2e53c-203">В случае проблемы это может быть использовано для вывода ошибки.</span><span class="sxs-lookup"><span data-stu-id="2e53c-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e53c-204">Требования</span><span class="sxs-lookup"><span data-stu-id="2e53c-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2e53c-205">Header</span><span class="sxs-lookup"><span data-stu-id="2e53c-205">Header</span></span></p></td><td><span data-ttu-id="2e53c-206">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="2e53c-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



