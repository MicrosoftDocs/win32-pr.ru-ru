---
title: Функция D3DX11CompileFromResource (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать функции ресурсов, а затем компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API D3DCompile. Компиляция шейдера или воздействия ресурса.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- D3DX11CompileFromResource функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000446"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="21e36-106">Функция D3DX11CompileFromResource</span><span class="sxs-lookup"><span data-stu-id="21e36-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="21e36-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="21e36-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="21e36-108">Вместо использования этой функции рекомендуется использовать [функции ресурсов](/windows/desktop/menurc/resources-functions), а затем компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="21e36-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="21e36-109">Компиляция шейдера или воздействия ресурса.</span><span class="sxs-lookup"><span data-stu-id="21e36-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e36-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21e36-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="21e36-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="21e36-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e36-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-113">Тип: **[ **хмодуле**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-114">Обработчик для модуля ресурсов, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="21e36-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="21e36-115">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="21e36-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="21e36-116">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-118">Имя ресурса, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="21e36-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="21e36-119">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="21e36-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="21e36-120">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="21e36-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-121">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-122">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="21e36-123">Optional.</span></span> <span data-ttu-id="21e36-124">Имя файла эффектов, которое используется только для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="21e36-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="21e36-125">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="21e36-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-126">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-127">Тип: **\* const [**D3D10ный \_ \_ макрос шейдера**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="21e36-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="21e36-128">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="21e36-128">Optional.</span></span> <span data-ttu-id="21e36-129">Указатель на массив определений макросов (см. раздел [**D3D10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="21e36-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="21e36-130">Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="21e36-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="21e36-131">Если не используется, задайте  для Пдефинес **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="21e36-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-132">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-133">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="21e36-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="21e36-134">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="21e36-134">Optional.</span></span> <span data-ttu-id="21e36-135">Указатель на интерфейс для обработки включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="21e36-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="21e36-136">Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.</span><span class="sxs-lookup"><span data-stu-id="21e36-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-137">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-138">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-139">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="21e36-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="21e36-140">При компиляции результата **D3DX11CompileFromResource** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="21e36-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-141">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-142">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-143">Строка, указывающая модель шейдера; может быть любым профилем в шейдере Model 2, Shader Model 3, Shader Model 4 или Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="21e36-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="21e36-144">Профиль также может иметь тип действия (например, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="21e36-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="21e36-145">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-146">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-147">[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-constants)шейдера.</span><span class="sxs-lookup"><span data-stu-id="21e36-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="21e36-148">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-149">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21e36-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21e36-150">[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)эффектов.</span><span class="sxs-lookup"><span data-stu-id="21e36-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="21e36-151">При компиляции шейдера, а не файла эффектов **D3DX11CompileFromResource** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="21e36-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-152">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e36-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-153">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="21e36-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="21e36-154">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="21e36-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="21e36-155">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="21e36-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-156">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="21e36-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-157">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="21e36-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="21e36-158">Указатель на память, которая содержит скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.</span><span class="sxs-lookup"><span data-stu-id="21e36-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-159">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="21e36-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-160">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="21e36-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="21e36-161">Указатель на память, которая содержит список ошибок и предупреждений, произошедших во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="21e36-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="21e36-162">Эти ошибки и предупреждения идентичны отладочным данным отладчика.</span><span class="sxs-lookup"><span data-stu-id="21e36-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="21e36-163">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="21e36-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21e36-164">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="21e36-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="21e36-165">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="21e36-165">A pointer to the return value.</span></span> <span data-ttu-id="21e36-166">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="21e36-166">May be **NULL**.</span></span> <span data-ttu-id="21e36-167">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="21e36-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e36-168">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21e36-168">Return value</span></span>

<span data-ttu-id="21e36-169">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21e36-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21e36-170">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="21e36-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="21e36-171">**D3DX11CompileFromResource** возвращает E \_ INVALIDARG, если параметр *фресулт* предоставляет значение, отличное от **null** , при указании **значения NULL** для параметра *ппумп* .</span><span class="sxs-lookup"><span data-stu-id="21e36-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="21e36-172">Дополнительные сведения об этой ситуации см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="21e36-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e36-173">Примечания</span><span class="sxs-lookup"><span data-stu-id="21e36-173">Remarks</span></span>

<span data-ttu-id="21e36-174">Дополнительные сведения о **D3DX11CompileFromResource** см. в разделе [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="21e36-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="21e36-175">Если параметру *ппумп* также присвоено **значение NULL** , необходимо указать **значение NULL** для параметра *фресулт* .</span><span class="sxs-lookup"><span data-stu-id="21e36-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="21e36-176">В противном случае вы не сможете создать шейдер с помощью скомпилированного кода шейдера, который **D3DX11CompileFromResource** возвращает в памяти, на которую указывает параметр *ппшадер* .</span><span class="sxs-lookup"><span data-stu-id="21e36-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="21e36-177">Чтобы создать шейдер из скомпилированного кода шейдера, необходимо вызвать один из следующих методов интерфейса [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="21e36-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="21e36-178">**креатекомпутешадер**</span><span class="sxs-lookup"><span data-stu-id="21e36-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="21e36-179">**креатедомаиншадер**</span><span class="sxs-lookup"><span data-stu-id="21e36-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="21e36-180">**креатежеометришадер**</span><span class="sxs-lookup"><span data-stu-id="21e36-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="21e36-181">**креатежеометришадервисстреамаутпут**</span><span class="sxs-lookup"><span data-stu-id="21e36-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="21e36-182">**креатехуллшадер**</span><span class="sxs-lookup"><span data-stu-id="21e36-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="21e36-183">**креатепикселшадер**</span><span class="sxs-lookup"><span data-stu-id="21e36-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="21e36-184">**креатевертексшадер**</span><span class="sxs-lookup"><span data-stu-id="21e36-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="21e36-185">Кроме того, если вы передаете значение, отличное от **null** , *фресулт* при указании значения **null** для *ппумп*, **D3DX11CompileFromResource** возвращает \_ код ошибки E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="21e36-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e36-186">Требования</span><span class="sxs-lookup"><span data-stu-id="21e36-186">Requirements</span></span>



| <span data-ttu-id="21e36-187">Требование</span><span class="sxs-lookup"><span data-stu-id="21e36-187">Requirement</span></span> | <span data-ttu-id="21e36-188">Значение</span><span class="sxs-lookup"><span data-stu-id="21e36-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e36-189">Header</span><span class="sxs-lookup"><span data-stu-id="21e36-189">Header</span></span><br/>  | <dl> <span data-ttu-id="21e36-190"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="21e36-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="21e36-191">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21e36-191">Library</span></span><br/> | <dl> <span data-ttu-id="21e36-192"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21e36-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="21e36-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21e36-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e36-194">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="21e36-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

