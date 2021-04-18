---
description: Создание обработчика асинхронных данных для воздействия.
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: Функция D3DX10CreateAsyncEffectCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713760"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="cbe84-103">Функция D3DX10CreateAsyncEffectCompilerProcessor</span><span class="sxs-lookup"><span data-stu-id="cbe84-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="cbe84-104">Создание обработчика асинхронных данных для воздействия.</span><span class="sxs-lookup"><span data-stu-id="cbe84-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbe84-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="cbe84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbe84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbe84-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbe84-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbe84-109">Строка, содержащая имя файла действия.</span><span class="sxs-lookup"><span data-stu-id="cbe84-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-110">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-111">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="cbe84-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="cbe84-112">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="cbe84-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-113">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-114">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="cbe84-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="cbe84-115">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="cbe84-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="cbe84-116">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cbe84-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-117">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbe84-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbe84-119">[Параметры компиляции HLSL](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cbe84-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-120">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbe84-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbe84-122">[Параметры компиляции эффектов](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="cbe84-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-123">*ппкомпиледшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-124">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="cbe84-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="cbe84-125">Адрес указателя на буфер (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="cbe84-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-126">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-127">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="cbe84-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="cbe84-128">Адрес указателя на буфер (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции.</span><span class="sxs-lookup"><span data-stu-id="cbe84-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="cbe84-129">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbe84-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe84-130">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cbe84-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="cbe84-131">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="cbe84-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbe84-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbe84-132">Return value</span></span>

<span data-ttu-id="cbe84-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cbe84-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cbe84-134">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cbe84-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe84-135">Требования</span><span class="sxs-lookup"><span data-stu-id="cbe84-135">Requirements</span></span>



| <span data-ttu-id="cbe84-136">Требование</span><span class="sxs-lookup"><span data-stu-id="cbe84-136">Requirement</span></span> | <span data-ttu-id="cbe84-137">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe84-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe84-138">Header</span><span class="sxs-lookup"><span data-stu-id="cbe84-138">Header</span></span><br/> | <dl> <span data-ttu-id="cbe84-139"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe84-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe84-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbe84-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe84-141">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="cbe84-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
