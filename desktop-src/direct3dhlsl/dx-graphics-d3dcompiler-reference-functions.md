---
title: Функции компилятора (Справочник по HLSL)
description: В этом разделе содержатся сведения о следующих функциях компилятора Direct3D HLSL.
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- функции, компилятор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee63fa17cc9216fdb92f69fed4d77bc65bb49048
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "104987410"
---
# <a name="compiler-functions-hlsl-reference"></a><span data-ttu-id="73623-104">Функции компилятора (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="73623-104">Compiler functions (HLSL reference)</span></span>

<span data-ttu-id="73623-105">В этом разделе содержатся сведения о следующих функциях компилятора Direct3D HLSL:</span><span class="sxs-lookup"><span data-stu-id="73623-105">This section contains information about the following Direct3D HLSL compiler functions:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="73623-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="73623-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73623-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="73623-107">Topic</span></span></th>
<th><span data-ttu-id="73623-108">Описание</span><span class="sxs-lookup"><span data-stu-id="73623-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73623-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-110">Возвращает указатель на интерфейс отражения.</span><span class="sxs-lookup"><span data-stu-id="73623-110">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-112">Скомпилируйте код HLSL или файл эффектов в байтах для заданного целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="73623-112">Compile HLSL code or an effect file into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-114">Компилирует код языка шейдера уровня Microsoft (HLSL) в байтовую кодировку для заданного целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="73623-114">Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="73623-116">Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="73623-116">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span> <span data-ttu-id="73623-117">См &quot; . раздел компиляция шейдеров для UWP &quot; в примечаниях для <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="73623-117">Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-118">Компилирует код HLSL в байтовые коды для заданного целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="73623-118">Compiles HLSL code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="73623-120">Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="73623-120">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-121">Сжимает набор шейдеров в более компактной форме.</span><span class="sxs-lookup"><span data-stu-id="73623-121">Compresses a set of shaders into a more compact form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-123">Создает буфер.</span><span class="sxs-lookup"><span data-stu-id="73623-123">Creates a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-125">Создает интерфейс взаимодействия между функциями и графами.</span><span class="sxs-lookup"><span data-stu-id="73623-125">Creates a function-linking-graph interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73623-126">Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="73623-126">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-128">Создает интерфейс компоновщика.</span><span class="sxs-lookup"><span data-stu-id="73623-128">Creates a linker interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73623-129">Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="73623-129">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="73623-131">Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="73623-131">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-132">Распаковывает один или несколько шейдеров из сжатого набора.</span><span class="sxs-lookup"><span data-stu-id="73623-132">Decompresses one or more shaders from a compressed set.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-134">Разборку скомпилированного кода HLSL.</span><span class="sxs-lookup"><span data-stu-id="73623-134">Disassembles compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-136">Разборку скомпилированного кода HLSL из Direct3D10ного действия.</span><span class="sxs-lookup"><span data-stu-id="73623-136">Disassembles compiled HLSL code from a Direct3D10 effect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-138">Разкомпилирует раздел скомпилированного кода HLSL, который указан в шагах трассировки шейдера.</span><span class="sxs-lookup"><span data-stu-id="73623-138">Disassembles a section of compiled HLSL code that is specified by shader trace steps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-140">Разборку определенной области скомпилированного кода HLSL.</span><span class="sxs-lookup"><span data-stu-id="73623-140">Disassembles a specific region of compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-142">Извлекает определенную часть из результата компиляции.</span><span class="sxs-lookup"><span data-stu-id="73623-142">Retrieves a specific part from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="73623-144">Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="73623-144">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-145">Получает отладочную информацию шейдера.</span><span class="sxs-lookup"><span data-stu-id="73623-145">Gets shader debug information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="73623-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="73623-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="73623-148">Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73623-148">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-149">Возвращает входные и выходные подписи из результата компиляции.</span><span class="sxs-lookup"><span data-stu-id="73623-149">Gets the input and output signatures from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-150">[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span><span class="sxs-lookup"><span data-stu-id="73623-150">[<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="73623-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="73623-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="73623-152">Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73623-152">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-153">Возвращает входную подпись из результата компиляции.</span><span class="sxs-lookup"><span data-stu-id="73623-153">Gets the input signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="73623-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="73623-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="73623-156">Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73623-156">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-157">Возвращает выходную подпись из результата компиляции.</span><span class="sxs-lookup"><span data-stu-id="73623-157">Gets the output signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-159">Возвращает смещение в байтах для инструкций в разделе кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="73623-159">Retrieves the byte offsets for instructions within a section of shader code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-161">Создает интерфейс модуля шейдера из исходных данных для модуля шейдера.</span><span class="sxs-lookup"><span data-stu-id="73623-161">Creates a shader module interface from source data for the shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73623-162">Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="73623-162">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-164">Предварительно обрабатывает некомпилированный код HLSL.</span><span class="sxs-lookup"><span data-stu-id="73623-164">Preprocesses uncompiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="73623-166">Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="73623-166">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-167">Считывает файл, который находится на диске, в память.</span><span class="sxs-lookup"><span data-stu-id="73623-167">Reads a file that is on disk into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-169">Возвращает указатель на интерфейс отражения.</span><span class="sxs-lookup"><span data-stu-id="73623-169">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-171">Создает интерфейс отражения библиотеки из исходных данных, который содержит HLSL библиотеку функций.</span><span class="sxs-lookup"><span data-stu-id="73623-171">Creates a library-reflection interface from source data that contains an HLSL library of functions.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73623-172">Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="73623-172">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-174">Задает сведения в результате компиляции.</span><span class="sxs-lookup"><span data-stu-id="73623-174">Sets information in a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73623-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="73623-176">Удаляет ненужные большие двоичные объекты из результата компиляции.</span><span class="sxs-lookup"><span data-stu-id="73623-176">Removes unwanted blobs from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73623-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="73623-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="73623-178">Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="73623-178">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="73623-179">Записывает большой двоичный объект памяти в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="73623-179">Writes a memory blob to a file on disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="73623-180">См. также</span><span class="sxs-lookup"><span data-stu-id="73623-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73623-181">Справочник по D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="73623-181">D3DCompiler Reference</span></span>](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

