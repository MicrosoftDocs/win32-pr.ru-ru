---
description: Примечание. вместо использования этой устаревшей функции рекомендуется использовать API D3DPreprocess. Создание шейдера из памяти без его компиляции.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: Функция D3DX10PreprocessShaderFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821317"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="3c045-104">Функция D3DX10PreprocessShaderFromMemory</span><span class="sxs-lookup"><span data-stu-id="3c045-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="3c045-105">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="3c045-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="3c045-106">Создание шейдера из памяти без его компиляции.</span><span class="sxs-lookup"><span data-stu-id="3c045-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c045-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c045-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="3c045-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c045-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c045-109">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c045-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c045-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c045-111">Указатель на память, содержащую шейдер.</span><span class="sxs-lookup"><span data-stu-id="3c045-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-112">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c045-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-113">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c045-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c045-114">Размер шейдера.</span><span class="sxs-lookup"><span data-stu-id="3c045-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-115">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c045-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-116">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c045-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c045-117">Имя шейдера.</span><span class="sxs-lookup"><span data-stu-id="3c045-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-118">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c045-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-119">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="3c045-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="3c045-120">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="3c045-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-121">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c045-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-122">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3c045-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="3c045-123">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="3c045-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-124">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c045-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-125">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c045-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="3c045-126">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="3c045-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="3c045-127">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="3c045-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-128">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3c045-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-129">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3c045-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3c045-130">Указатель на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), содержащий некомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="3c045-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-131">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3c045-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c045-132">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3c045-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3c045-133">Адрес указателя на память (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит ошибки создания эффектов, если таковые возникли.</span><span class="sxs-lookup"><span data-stu-id="3c045-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c045-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c045-134">Return value</span></span>

<span data-ttu-id="3c045-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c045-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c045-136">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3c045-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c045-137">Требования</span><span class="sxs-lookup"><span data-stu-id="3c045-137">Requirements</span></span>



| <span data-ttu-id="3c045-138">Требование</span><span class="sxs-lookup"><span data-stu-id="3c045-138">Requirement</span></span> | <span data-ttu-id="3c045-139">Значение</span><span class="sxs-lookup"><span data-stu-id="3c045-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c045-140">Header</span><span class="sxs-lookup"><span data-stu-id="3c045-140">Header</span></span><br/>  | <dl> <span data-ttu-id="3c045-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c045-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c045-142">Library</span></span><br/> | <dl> <span data-ttu-id="3c045-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c045-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c045-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c045-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c045-145">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="3c045-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
