---
description: Примечание. вместо использования этой устаревшей функции рекомендуется использовать API D3DPreprocess. Создание шейдера из файла без его компиляции.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: Функция D3DX10PreprocessShaderFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713853"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="a88c3-104">Функция D3DX10PreprocessShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="a88c3-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="a88c3-105">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="a88c3-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="a88c3-106">Создание шейдера из файла без его компиляции.</span><span class="sxs-lookup"><span data-stu-id="a88c3-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a88c3-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="a88c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a88c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88c3-109">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c3-110">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a88c3-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a88c3-111">Имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="a88c3-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="a88c3-112">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c3-113">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="a88c3-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a88c3-114">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="a88c3-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a88c3-115">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c3-116">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a88c3-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a88c3-117">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="a88c3-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="a88c3-118">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c3-119">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a88c3-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="a88c3-120">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a88c3-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="a88c3-121">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="a88c3-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="a88c3-122">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c3-123">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a88c3-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a88c3-124">Указатель на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), содержащий некомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="a88c3-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="a88c3-125">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c3-126">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a88c3-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a88c3-127">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки создания эффектов, если таковые возникли.</span><span class="sxs-lookup"><span data-stu-id="a88c3-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88c3-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a88c3-128">Return value</span></span>

<span data-ttu-id="a88c3-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a88c3-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a88c3-130">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a88c3-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a88c3-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a88c3-131">Requirements</span></span>



| <span data-ttu-id="a88c3-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a88c3-132">Requirement</span></span> | <span data-ttu-id="a88c3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a88c3-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88c3-134">Header</span><span class="sxs-lookup"><span data-stu-id="a88c3-134">Header</span></span><br/> | <dl> <span data-ttu-id="a88c3-135"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a88c3-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88c3-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a88c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88c3-137">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="a88c3-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
