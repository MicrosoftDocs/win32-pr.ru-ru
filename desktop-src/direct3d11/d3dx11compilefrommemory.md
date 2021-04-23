---
title: Функция D3DX11CompileFromMemory (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API D3DCompile. Скомпилируйте шейдер или результат, который загружается в память.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- D3DX11CompileFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987032"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="46843-106">Функция D3DX11CompileFromMemory</span><span class="sxs-lookup"><span data-stu-id="46843-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="46843-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="46843-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="46843-108">Вместо использования этой функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="46843-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="46843-109">Скомпилируйте шейдер или результат, который загружается в память.</span><span class="sxs-lookup"><span data-stu-id="46843-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="46843-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46843-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="46843-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="46843-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46843-112">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-113">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-114">Указатель на шейдер в памяти.</span><span class="sxs-lookup"><span data-stu-id="46843-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="46843-115">*Сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-116">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-117">Размер шейдера в памяти.</span><span class="sxs-lookup"><span data-stu-id="46843-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="46843-118">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-119">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-120">Имя файла, содержащего код шейдера.</span><span class="sxs-lookup"><span data-stu-id="46843-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="46843-121">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-122">Тип: **\* const [**D3D10ный \_ \_ макрос шейдера**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="46843-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="46843-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="46843-123">Optional.</span></span> <span data-ttu-id="46843-124">Указатель на массив определений макросов (см. раздел [**D3D10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="46843-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="46843-125">Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="46843-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="46843-126">Если не используется, задайте  для Пдефинес **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="46843-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="46843-127">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-128">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="46843-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="46843-129">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="46843-129">Optional.</span></span> <span data-ttu-id="46843-130">Указатель на интерфейс для обработки включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="46843-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="46843-131">Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.</span><span class="sxs-lookup"><span data-stu-id="46843-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="46843-132">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-133">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-134">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="46843-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="46843-135">При компиляции результата **D3DX11CompileFromMemory** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="46843-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="46843-136">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-137">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-138">Строка, указывающая модель шейдера; может быть любым профилем в шейдере Model 2, Shader Model 3, Shader Model 4 или Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="46843-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="46843-139">Профиль также может иметь тип действия (например, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="46843-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="46843-140">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-141">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-142">[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-constants)шейдера.</span><span class="sxs-lookup"><span data-stu-id="46843-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="46843-143">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-144">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46843-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46843-145">[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)эффектов.</span><span class="sxs-lookup"><span data-stu-id="46843-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="46843-146">При компиляции шейдера, а не файла эффектов **D3DX11CompileFromMemory** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="46843-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="46843-147">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46843-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-148">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="46843-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="46843-149">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="46843-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="46843-150">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="46843-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="46843-151">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46843-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-152">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="46843-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="46843-153">Указатель на память, которая содержит скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.</span><span class="sxs-lookup"><span data-stu-id="46843-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="46843-154">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46843-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-155">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="46843-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="46843-156">Указатель на память, которая содержит список ошибок и предупреждений, произошедших во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="46843-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="46843-157">Эти ошибки и предупреждения идентичны отладочным данным отладчика.</span><span class="sxs-lookup"><span data-stu-id="46843-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="46843-158">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46843-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46843-159">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="46843-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="46843-160">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="46843-160">A pointer to the return value.</span></span> <span data-ttu-id="46843-161">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="46843-161">May be **NULL**.</span></span> <span data-ttu-id="46843-162">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="46843-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46843-163">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46843-163">Return value</span></span>

<span data-ttu-id="46843-164">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46843-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46843-165">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="46843-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="46843-166">**D3DX11CompileFromMemory** возвращает E \_ INVALIDARG, если параметр *фресулт* предоставляет значение, отличное от **null** , при указании **значения NULL** для параметра *ппумп* .</span><span class="sxs-lookup"><span data-stu-id="46843-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="46843-167">Дополнительные сведения об этой ситуации см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="46843-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="46843-168">Примечания</span><span class="sxs-lookup"><span data-stu-id="46843-168">Remarks</span></span>

<span data-ttu-id="46843-169">Дополнительные сведения о **D3DX11CompileFromMemory** см. в разделе [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="46843-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="46843-170">Если параметру *ппумп* также присвоено **значение NULL** , необходимо указать **значение NULL** для параметра *фресулт* .</span><span class="sxs-lookup"><span data-stu-id="46843-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="46843-171">В противном случае вы не сможете создать шейдер с помощью скомпилированного кода шейдера, который **D3DX11CompileFromMemory** возвращает в памяти, на которую указывает параметр *ппшадер* .</span><span class="sxs-lookup"><span data-stu-id="46843-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="46843-172">Чтобы создать шейдер из скомпилированного кода шейдера, необходимо вызвать один из следующих методов интерфейса [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="46843-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="46843-173">**креатекомпутешадер**</span><span class="sxs-lookup"><span data-stu-id="46843-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="46843-174">**креатедомаиншадер**</span><span class="sxs-lookup"><span data-stu-id="46843-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="46843-175">**креатежеометришадер**</span><span class="sxs-lookup"><span data-stu-id="46843-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="46843-176">**креатежеометришадервисстреамаутпут**</span><span class="sxs-lookup"><span data-stu-id="46843-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="46843-177">**креатехуллшадер**</span><span class="sxs-lookup"><span data-stu-id="46843-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="46843-178">**креатепикселшадер**</span><span class="sxs-lookup"><span data-stu-id="46843-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="46843-179">**креатевертексшадер**</span><span class="sxs-lookup"><span data-stu-id="46843-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="46843-180">Кроме того, если вы передаете значение, отличное от **null** , *фресулт* при указании значения **null** для *ппумп*, **D3DX11CompileFromMemory** возвращает \_ код ошибки E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="46843-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="46843-181">Требования</span><span class="sxs-lookup"><span data-stu-id="46843-181">Requirements</span></span>



| <span data-ttu-id="46843-182">Требование</span><span class="sxs-lookup"><span data-stu-id="46843-182">Requirement</span></span> | <span data-ttu-id="46843-183">Значение</span><span class="sxs-lookup"><span data-stu-id="46843-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46843-184">Header</span><span class="sxs-lookup"><span data-stu-id="46843-184">Header</span></span><br/>  | <dl> <span data-ttu-id="46843-185"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="46843-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="46843-186">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46843-186">Library</span></span><br/> | <dl> <span data-ttu-id="46843-187"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46843-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="46843-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46843-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46843-189">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="46843-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

