---
description: Примечание. вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API D3DCompile. Компиляция шейдера или воздействия ресурса.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: Функция D3DX10CompileFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713588"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="79869-104">Функция D3DX10CompileFromResource</span><span class="sxs-lookup"><span data-stu-id="79869-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="79869-105">Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="79869-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="79869-106">Компиляция шейдера или воздействия ресурса.</span><span class="sxs-lookup"><span data-stu-id="79869-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="79869-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79869-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="79869-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79869-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79869-109">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-110">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-111">Обработчик для модуля ресурсов, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="79869-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="79869-112">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="79869-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="79869-113">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-114">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-115">Имя ресурса, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="79869-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="79869-116">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="79869-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="79869-117">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="79869-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="79869-118">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-119">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="79869-120">Optional.</span></span> <span data-ttu-id="79869-121">Имя файла эффектов, которое используется только для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="79869-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="79869-122">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="79869-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="79869-123">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-124">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="79869-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="79869-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="79869-125">Optional.</span></span> <span data-ttu-id="79869-126">Указатель на массив определений макросов (см. [**\_ \_ макрос D3D Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="79869-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="79869-127">Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="79869-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="79869-128">Если не используется, задайте  для Пдефинес **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="79869-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="79869-129">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-130">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="79869-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="79869-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="79869-131">Optional.</span></span> <span data-ttu-id="79869-132">Указатель на интерфейс интерфейса [**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) для обработки включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="79869-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="79869-133">Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.</span><span class="sxs-lookup"><span data-stu-id="79869-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="79869-134">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-135">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-136">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="79869-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="79869-137">При компиляции результата **D3DX10CompileFromResource** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="79869-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="79869-138">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-139">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-140">Строка, указывающая модель шейдера; может быть любым профилем в [шейдере Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)или [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="79869-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="79869-141">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-142">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-143">[Флаги компиляции шейдера](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="79869-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="79869-144">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-145">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79869-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79869-146">[Флаги компиляции эффектов](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="79869-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="79869-147">При компиляции шейдера, а не файла эффектов **D3DX10CompileFromResource** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="79869-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="79869-148">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79869-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-149">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="79869-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="79869-150">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="79869-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="79869-151">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="79869-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="79869-152">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79869-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-153">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="79869-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="79869-154">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.</span><span class="sxs-lookup"><span data-stu-id="79869-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="79869-155">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79869-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-156">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="79869-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="79869-157">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий список ошибок и предупреждений, произошедших во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="79869-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="79869-158">Эти ошибки и предупреждения идентичны отладочным данным отладчика.</span><span class="sxs-lookup"><span data-stu-id="79869-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="79869-159">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79869-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79869-160">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="79869-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="79869-161">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="79869-161">A pointer to the return value.</span></span> <span data-ttu-id="79869-162">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="79869-162">May be **NULL**.</span></span> <span data-ttu-id="79869-163">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="79869-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79869-164">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79869-164">Return value</span></span>

<span data-ttu-id="79869-165">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79869-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79869-166">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="79869-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79869-167">Требования</span><span class="sxs-lookup"><span data-stu-id="79869-167">Requirements</span></span>



| <span data-ttu-id="79869-168">Требование</span><span class="sxs-lookup"><span data-stu-id="79869-168">Requirement</span></span> | <span data-ttu-id="79869-169">Значение</span><span class="sxs-lookup"><span data-stu-id="79869-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79869-170">Header</span><span class="sxs-lookup"><span data-stu-id="79869-170">Header</span></span><br/> | <dl> <span data-ttu-id="79869-171"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="79869-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79869-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79869-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79869-173">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="79869-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
