---
description: Создайте обработчик асинхронных данных для шейдера.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Функция D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273739"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="e0fbf-103">Функция D3DX10CreateAsyncCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="e0fbf-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="e0fbf-104">Создайте обработчик асинхронных данных для шейдера.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0fbf-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="e0fbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0fbf-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0fbf-109">Строка, содержащая имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-110">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-111">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="e0fbf-112">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-113">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-114">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="e0fbf-115">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="e0fbf-116">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-117">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-118">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0fbf-119">Имя функции-точки входа шейдера, где начинается выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="e0fbf-120">При компиляции результата **D3DX10CreateAsyncCompilerProcessor** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-121">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-122">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0fbf-123">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md) или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-124">*Flags1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-125">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0fbf-126">[Флаги компиляции шейдера](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-127">*Flags2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-128">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0fbf-129">[Флаги компиляции эффектов](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="e0fbf-130">При компиляции шейдера, а не файла эффектов **D3DX10CreateAsyncCompilerProcessor** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="e0fbf-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-131">*ппкомпиледшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-132">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0fbf-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e0fbf-133">Адрес указателя на скомпилированный результат (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-134">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-135">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0fbf-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e0fbf-136">Адрес указателя для ошибок компиляции (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="e0fbf-137">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0fbf-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbf-138">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0fbf-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="e0fbf-139">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0fbf-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0fbf-140">Return value</span></span>

<span data-ttu-id="e0fbf-141">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0fbf-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0fbf-142">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e0fbf-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fbf-143">Требования</span><span class="sxs-lookup"><span data-stu-id="e0fbf-143">Requirements</span></span>



| <span data-ttu-id="e0fbf-144">Требование</span><span class="sxs-lookup"><span data-stu-id="e0fbf-144">Requirement</span></span> | <span data-ttu-id="e0fbf-145">Значение</span><span class="sxs-lookup"><span data-stu-id="e0fbf-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fbf-146">Header</span><span class="sxs-lookup"><span data-stu-id="e0fbf-146">Header</span></span><br/> | <dl> <span data-ttu-id="e0fbf-147"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0fbf-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fbf-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0fbf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fbf-149">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="e0fbf-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
