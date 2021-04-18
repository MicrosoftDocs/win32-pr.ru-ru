---
description: Примечание. вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API D3DCompile. Скомпилируйте шейдер или результат из файла.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: Функция D3DX10CompileFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713921"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="fc452-104">Функция D3DX10CompileFromFile</span><span class="sxs-lookup"><span data-stu-id="fc452-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="fc452-105">Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="fc452-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="fc452-106">Скомпилируйте шейдер или результат из файла.</span><span class="sxs-lookup"><span data-stu-id="fc452-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc452-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc452-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="fc452-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc452-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc452-109">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-110">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc452-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc452-111">Имя файла, содержащего код шейдера.</span><span class="sxs-lookup"><span data-stu-id="fc452-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="fc452-112">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="fc452-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fc452-113">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fc452-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-114">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-115">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="fc452-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="fc452-116">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fc452-116">Optional.</span></span> <span data-ttu-id="fc452-117">Указатель на массив определений макросов (см. [**\_ \_ макрос D3D Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="fc452-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="fc452-118">Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="fc452-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="fc452-119">Если не используется, задайте  для Пдефинес **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc452-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-120">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-121">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="fc452-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="fc452-122">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fc452-122">Optional.</span></span> <span data-ttu-id="fc452-123">Указатель на интерфейс интерфейса [**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) для обработки включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="fc452-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="fc452-124">Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.</span><span class="sxs-lookup"><span data-stu-id="fc452-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-125">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-126">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc452-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc452-127">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="fc452-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="fc452-128">При компиляции результата **D3DX10CompileFromFile** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="fc452-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-129">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-130">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc452-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc452-131">Строка, указывающая модель шейдера; может быть любым профилем в [шейдере Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)или [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="fc452-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc452-132">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-133">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc452-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc452-134">[Флаги компиляции шейдера](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="fc452-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc452-135">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-136">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc452-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc452-137">[Флаги компиляции эффектов](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fc452-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="fc452-138">При компиляции шейдера, а не файла эффектов **D3DX10CompileFromFile** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="fc452-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-139">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc452-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-140">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc452-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="fc452-141">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="fc452-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="fc452-142">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="fc452-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-143">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc452-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-144">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fc452-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fc452-145">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.</span><span class="sxs-lookup"><span data-stu-id="fc452-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-146">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc452-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-147">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fc452-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fc452-148">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий список ошибок и предупреждений, произошедших во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="fc452-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="fc452-149">Эти ошибки и предупреждения идентичны отладочным данным отладчика.</span><span class="sxs-lookup"><span data-stu-id="fc452-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="fc452-150">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc452-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc452-151">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="fc452-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="fc452-152">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="fc452-152">A pointer to the return value.</span></span> <span data-ttu-id="fc452-153">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc452-153">May be **NULL**.</span></span> <span data-ttu-id="fc452-154">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="fc452-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc452-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc452-155">Return value</span></span>

<span data-ttu-id="fc452-156">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc452-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc452-157">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fc452-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc452-158">Remarks</span><span class="sxs-lookup"><span data-stu-id="fc452-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fc452-159">Требования</span><span class="sxs-lookup"><span data-stu-id="fc452-159">Requirements</span></span>



| <span data-ttu-id="fc452-160">Требование</span><span class="sxs-lookup"><span data-stu-id="fc452-160">Requirement</span></span> | <span data-ttu-id="fc452-161">Значение</span><span class="sxs-lookup"><span data-stu-id="fc452-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc452-162">Header</span><span class="sxs-lookup"><span data-stu-id="fc452-162">Header</span></span><br/> | <dl> <span data-ttu-id="fc452-163"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc452-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc452-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc452-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc452-165">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="fc452-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
