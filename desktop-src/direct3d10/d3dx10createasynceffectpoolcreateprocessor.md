---
description: Создайте обработчик асинхронных данных для пула памяти.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: Функция D3DX10CreateAsyncEffectPoolCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273836"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="b35d7-103">Функция D3DX10CreateAsyncEffectPoolCreateProcessor</span><span class="sxs-lookup"><span data-stu-id="b35d7-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="b35d7-104">Создайте обработчик асинхронных данных для пула памяти.</span><span class="sxs-lookup"><span data-stu-id="b35d7-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b35d7-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="b35d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b35d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b35d7-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35d7-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b35d7-109">Строка, содержащая имя файла действия.</span><span class="sxs-lookup"><span data-stu-id="b35d7-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-110">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-111">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="b35d7-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="b35d7-112">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="b35d7-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-113">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-114">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b35d7-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="b35d7-115">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="b35d7-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-116">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-117">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35d7-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b35d7-118">Строка, указывающая [профиль шейдера](../direct3dhlsl/dx-graphics-hlsl-models.md) или модель шейдера.</span><span class="sxs-lookup"><span data-stu-id="b35d7-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-119">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35d7-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b35d7-121">Параметры компиляции HLSL (см. раздел [Флаги шейдеров](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="b35d7-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-122">*Фксфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35d7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b35d7-124">Параметры компиляции эффектов (см. раздел [флаги компиляции и влияния](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="b35d7-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-125">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-126">Тип: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="b35d7-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="b35d7-127">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b35d7-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-128">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-129">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b35d7-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b35d7-130">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки компиляции эффектов, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="b35d7-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="b35d7-131">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b35d7-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b35d7-132">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b35d7-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="b35d7-133">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="b35d7-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b35d7-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b35d7-134">Return value</span></span>

<span data-ttu-id="b35d7-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b35d7-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b35d7-136">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b35d7-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b35d7-137">Требования</span><span class="sxs-lookup"><span data-stu-id="b35d7-137">Requirements</span></span>



| <span data-ttu-id="b35d7-138">Требование</span><span class="sxs-lookup"><span data-stu-id="b35d7-138">Requirement</span></span> | <span data-ttu-id="b35d7-139">Значение</span><span class="sxs-lookup"><span data-stu-id="b35d7-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35d7-140">Header</span><span class="sxs-lookup"><span data-stu-id="b35d7-140">Header</span></span><br/> | <dl> <span data-ttu-id="b35d7-141"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="b35d7-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b35d7-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b35d7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35d7-143">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="b35d7-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
