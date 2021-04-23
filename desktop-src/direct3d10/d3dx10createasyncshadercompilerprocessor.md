---
description: Скомпилируйте шейдер и создайте обработчик данных в асинхронном режиме.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: Функция D3DX10CreateAsyncShaderCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424362"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="80493-103">Функция D3DX10CreateAsyncShaderCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="80493-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="80493-104">Скомпилируйте шейдер и создайте обработчик данных в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="80493-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="80493-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80493-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="80493-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80493-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80493-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80493-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80493-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80493-109">Строка, содержащая имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="80493-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="80493-110">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80493-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-111">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="80493-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="80493-112">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="80493-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="80493-113">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80493-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-114">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="80493-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="80493-115">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="80493-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="80493-116">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80493-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-117">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80493-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80493-118">Имя функции точки входа для шейдера.</span><span class="sxs-lookup"><span data-stu-id="80493-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="80493-119">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80493-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-120">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80493-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80493-121">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md) или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="80493-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="80493-122">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80493-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80493-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80493-124">Параметры компиляции HLSL (см. раздел [Флаги шейдеров](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="80493-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="80493-125">*ппкомпиледшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80493-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-126">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="80493-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="80493-127">Адрес указателя на скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="80493-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="80493-128">См. раздел [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="80493-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="80493-129">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80493-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-130">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="80493-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="80493-131">Адрес указателя на буфер, содержащий ошибки компиляции (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="80493-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="80493-132">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80493-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80493-133">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="80493-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="80493-134">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="80493-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80493-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80493-135">Return value</span></span>

<span data-ttu-id="80493-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80493-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80493-137">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="80493-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80493-138">Требования</span><span class="sxs-lookup"><span data-stu-id="80493-138">Requirements</span></span>



| <span data-ttu-id="80493-139">Требование</span><span class="sxs-lookup"><span data-stu-id="80493-139">Requirement</span></span> | <span data-ttu-id="80493-140">Значение</span><span class="sxs-lookup"><span data-stu-id="80493-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80493-141">Header</span><span class="sxs-lookup"><span data-stu-id="80493-141">Header</span></span><br/> | <dl> <span data-ttu-id="80493-142"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="80493-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80493-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80493-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80493-144">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="80493-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
