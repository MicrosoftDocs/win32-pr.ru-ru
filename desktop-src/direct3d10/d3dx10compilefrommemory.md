---
description: Примечание. вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API D3DCompile. Скомпилируйте шейдер или результат, который загружается в память.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Функция D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: fbb4a716df4a893ea122e7badfd6faad536aacce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000485"
---
# <a name="d3dx10compilefrommemory-function"></a><span data-ttu-id="1677b-104">Функция D3DX10CompileFromMemory</span><span class="sxs-lookup"><span data-stu-id="1677b-104">D3DX10CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="1677b-105">Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="1677b-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="1677b-106">Скомпилируйте шейдер или результат, который загружается в память.</span><span class="sxs-lookup"><span data-stu-id="1677b-106">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1677b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1677b-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="1677b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1677b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1677b-109">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-111">Указатель на шейдер в памяти.</span><span class="sxs-lookup"><span data-stu-id="1677b-111">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-112">*Сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-112">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-113">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-114">Размер шейдера в памяти.</span><span class="sxs-lookup"><span data-stu-id="1677b-114">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-115">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-116">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-117">Имя файла, содержащего код шейдера.</span><span class="sxs-lookup"><span data-stu-id="1677b-117">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-118">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-119">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="1677b-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1677b-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1677b-120">Optional.</span></span> <span data-ttu-id="1677b-121">Указатель на массив определений макросов (см. [**\_ \_ макрос D3D Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="1677b-121">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="1677b-122">Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="1677b-122">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="1677b-123">Если не используется, задайте  для Пдефинес **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1677b-123">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-124">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-125">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1677b-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="1677b-126">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1677b-126">Optional.</span></span> <span data-ttu-id="1677b-127">Указатель на интерфейс интерфейса [**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) для обработки включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="1677b-127">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="1677b-128">Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.</span><span class="sxs-lookup"><span data-stu-id="1677b-128">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-129">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-129">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-130">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-131">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="1677b-131">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="1677b-132">При компиляции результата **D3DX10CompileFromMemory** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="1677b-132">When you compile an effect, **D3DX10CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-133">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-133">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-134">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-134">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-135">Строка, указывающая модель шейдера; может быть любым профилем в [шейдере Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)или [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="1677b-135">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="1677b-136">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-137">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-138">[Флаги компиляции шейдера](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="1677b-138">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="1677b-139">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-140">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1677b-140">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1677b-141">[Флаги компиляции эффектов](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1677b-141">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="1677b-142">При компиляции шейдера, а не файла эффектов **D3DX10CompileFromMemory** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="1677b-142">When you compile a shader and not an effect file, **D3DX10CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-143">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1677b-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-144">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1677b-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1677b-145">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1677b-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1677b-146">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="1677b-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-147">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1677b-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-148">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1677b-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1677b-149">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.</span><span class="sxs-lookup"><span data-stu-id="1677b-149">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-150">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1677b-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-151">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1677b-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1677b-152">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий список ошибок и предупреждений, произошедших во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="1677b-152">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="1677b-153">Эти ошибки и предупреждения идентичны отладочным данным отладчика.</span><span class="sxs-lookup"><span data-stu-id="1677b-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="1677b-154">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1677b-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1677b-155">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1677b-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1677b-156">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="1677b-156">A pointer to the return value.</span></span> <span data-ttu-id="1677b-157">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1677b-157">May be **NULL**.</span></span> <span data-ttu-id="1677b-158">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="1677b-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1677b-159">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1677b-159">Return value</span></span>

<span data-ttu-id="1677b-160">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1677b-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1677b-161">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1677b-161">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1677b-162">Требования</span><span class="sxs-lookup"><span data-stu-id="1677b-162">Requirements</span></span>



| <span data-ttu-id="1677b-163">Требование</span><span class="sxs-lookup"><span data-stu-id="1677b-163">Requirement</span></span> | <span data-ttu-id="1677b-164">Значение</span><span class="sxs-lookup"><span data-stu-id="1677b-164">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1677b-165">Header</span><span class="sxs-lookup"><span data-stu-id="1677b-165">Header</span></span><br/> | <dl> <span data-ttu-id="1677b-166"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1677b-166"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1677b-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1677b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1677b-168">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="1677b-168">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
