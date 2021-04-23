---
title: Функция D3DX11CompileFromFile (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API D3DCompileFromFile. Скомпилируйте шейдер или результат из файла.
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- D3DX11CompileFromFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157219"
---
# <a name="d3dx11compilefromfile-function"></a><span data-ttu-id="d69c6-106">Функция D3DX11CompileFromFile</span><span class="sxs-lookup"><span data-stu-id="d69c6-106">D3DX11CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="d69c6-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="d69c6-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="d69c6-108">Вместо использования этой функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="d69c6-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API.</span></span>

 

<span data-ttu-id="d69c6-109">Скомпилируйте шейдер или результат из файла.</span><span class="sxs-lookup"><span data-stu-id="d69c6-109">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69c6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d69c6-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="d69c6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d69c6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d69c6-112">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-113">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d69c6-114">Имя файла, содержащего код шейдера.</span><span class="sxs-lookup"><span data-stu-id="d69c6-114">The name of the file that contains the shader code.</span></span> <span data-ttu-id="d69c6-115">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="d69c6-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d69c6-116">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d69c6-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-117">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-118">Тип: **\* const [**D3D10ный \_ \_ макрос шейдера**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-118">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d69c6-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d69c6-119">Optional.</span></span> <span data-ttu-id="d69c6-120">Указатель на массив определений макросов (см. раздел [**D3D10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="d69c6-120">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="d69c6-121">Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="d69c6-121">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="d69c6-122">Если не используется, задайте  для Пдефинес **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d69c6-122">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-123">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-124">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d69c6-124">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d69c6-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d69c6-125">Optional.</span></span> <span data-ttu-id="d69c6-126">Указатель на интерфейс для обработки включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="d69c6-126">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="d69c6-127">Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.</span><span class="sxs-lookup"><span data-stu-id="d69c6-127">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-128">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-128">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-129">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-129">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d69c6-130">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="d69c6-130">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="d69c6-131">При компиляции результата **D3DX11CompileFromFile** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="d69c6-131">When you compile an effect, **D3DX11CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-132">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-132">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-133">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d69c6-134">Строка, указывающая модель шейдера; может быть любым профилем в шейдере Model 2, Shader Model 3, Shader Model 4 или Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="d69c6-134">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="d69c6-135">Профиль также может иметь тип действия (например, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="d69c6-135">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-136">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-137">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-137">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d69c6-138">[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-constants)шейдера.</span><span class="sxs-lookup"><span data-stu-id="d69c6-138">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-139">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-140">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-140">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d69c6-141">[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)эффектов.</span><span class="sxs-lookup"><span data-stu-id="d69c6-141">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="d69c6-142">При компиляции шейдера, а не файла эффектов **D3DX11CompileFromFile** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="d69c6-142">When you compile a shader and not an effect file, **D3DX11CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-143">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-144">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d69c6-144">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="d69c6-145">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d69c6-145">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="d69c6-146">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="d69c6-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-147">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-148">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d69c6-148">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d69c6-149">Указатель на память, которая содержит скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.</span><span class="sxs-lookup"><span data-stu-id="d69c6-149">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-150">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-151">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d69c6-151">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d69c6-152">Указатель на память, которая содержит список ошибок и предупреждений, произошедших во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="d69c6-152">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="d69c6-153">Эти ошибки и предупреждения идентичны отладочным данным отладчика.</span><span class="sxs-lookup"><span data-stu-id="d69c6-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="d69c6-154">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d69c6-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c6-155">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d69c6-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d69c6-156">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="d69c6-156">A pointer to the return value.</span></span> <span data-ttu-id="d69c6-157">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d69c6-157">May be **NULL**.</span></span> <span data-ttu-id="d69c6-158">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="d69c6-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d69c6-159">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d69c6-159">Return value</span></span>

<span data-ttu-id="d69c6-160">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d69c6-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d69c6-161">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d69c6-161">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="d69c6-162">**D3DX11CompileFromFile** возвращает E \_ INVALIDARG, если параметр *фресулт* предоставляет значение, отличное от **null** , при указании значения **null** для параметра *ппумп* .</span><span class="sxs-lookup"><span data-stu-id="d69c6-162">**D3DX11CompileFromFile** returns E\_INVALIDARG if you supply a non-**NULL** value to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="d69c6-163">Дополнительные сведения об этой ситуации см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="d69c6-163">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="d69c6-164">Примечания</span><span class="sxs-lookup"><span data-stu-id="d69c6-164">Remarks</span></span>

<span data-ttu-id="d69c6-165">Дополнительные сведения о **D3DX11CompileFromFile** см. в разделе [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="d69c6-165">For more information about **D3DX11CompileFromFile**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="d69c6-166">Если параметру *ппумп* также присвоено **значение NULL** , необходимо указать **значение NULL** для параметра *фресулт* .</span><span class="sxs-lookup"><span data-stu-id="d69c6-166">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="d69c6-167">В противном случае нельзя создать шейдер с помощью скомпилированного кода шейдера, который **D3DX11CompileFromFile** возвращает в памяти, на которую указывает параметр *ппшадер* .</span><span class="sxs-lookup"><span data-stu-id="d69c6-167">Otherwise, you cannot create a shader by using the compiled shader code that **D3DX11CompileFromFile** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="d69c6-168">Чтобы создать шейдер из скомпилированного кода шейдера, необходимо вызвать один из следующих методов интерфейса [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="d69c6-168">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="d69c6-169">**креатекомпутешадер**</span><span class="sxs-lookup"><span data-stu-id="d69c6-169">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="d69c6-170">**креатедомаиншадер**</span><span class="sxs-lookup"><span data-stu-id="d69c6-170">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="d69c6-171">**креатежеометришадер**</span><span class="sxs-lookup"><span data-stu-id="d69c6-171">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="d69c6-172">**креатежеометришадервисстреамаутпут**</span><span class="sxs-lookup"><span data-stu-id="d69c6-172">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="d69c6-173">**креатехуллшадер**</span><span class="sxs-lookup"><span data-stu-id="d69c6-173">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="d69c6-174">**креатепикселшадер**</span><span class="sxs-lookup"><span data-stu-id="d69c6-174">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="d69c6-175">**креатевертексшадер**</span><span class="sxs-lookup"><span data-stu-id="d69c6-175">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="d69c6-176">Кроме того, если вы передаете значение, отличное от **null** , *фресулт* при указании значения **null** для *ппумп*, **D3DX11CompileFromFile** возвращает \_ код ошибки E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d69c6-176">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromFile** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69c6-177">Требования</span><span class="sxs-lookup"><span data-stu-id="d69c6-177">Requirements</span></span>



| <span data-ttu-id="d69c6-178">Требование</span><span class="sxs-lookup"><span data-stu-id="d69c6-178">Requirement</span></span> | <span data-ttu-id="d69c6-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d69c6-179">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69c6-180">Header</span><span class="sxs-lookup"><span data-stu-id="d69c6-180">Header</span></span><br/>  | <dl> <span data-ttu-id="d69c6-181"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69c6-181"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="d69c6-182">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d69c6-182">Library</span></span><br/> | <dl> <span data-ttu-id="d69c6-183"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d69c6-183"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d69c6-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d69c6-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69c6-185">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="d69c6-185">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

