---
title: Функция D3DX11PreprocessShaderFromMemory (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать API D3DPreprocess. Создание шейдера из памяти без его компиляции.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- D3DX11PreprocessShaderFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998504"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="88db9-106">Функция D3DX11PreprocessShaderFromMemory</span><span class="sxs-lookup"><span data-stu-id="88db9-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="88db9-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="88db9-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="88db9-108">Вместо использования этой функции рекомендуется использовать API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="88db9-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="88db9-109">Создание шейдера из памяти без его компиляции.</span><span class="sxs-lookup"><span data-stu-id="88db9-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="88db9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88db9-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="88db9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="88db9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88db9-112">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88db9-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-113">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="88db9-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="88db9-114">Указатель на память, содержащую шейдер.</span><span class="sxs-lookup"><span data-stu-id="88db9-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-115">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88db9-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-116">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="88db9-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="88db9-117">Размер шейдера.</span><span class="sxs-lookup"><span data-stu-id="88db9-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-118">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88db9-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-119">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="88db9-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="88db9-120">Имя шейдера.</span><span class="sxs-lookup"><span data-stu-id="88db9-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-121">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88db9-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-122">Тип: **const D3D11ный \_ \_ макрос \* шейдера**</span><span class="sxs-lookup"><span data-stu-id="88db9-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="88db9-123">Массив макросов шейдеров, заканчивающийся нулем; Установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="88db9-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-124">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88db9-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-125">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="88db9-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="88db9-126">Указатель на интерфейс include; Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="88db9-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-127">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88db9-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-128">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="88db9-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="88db9-129">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="88db9-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="88db9-130">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="88db9-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-131">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88db9-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-132">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="88db9-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="88db9-133">Указатель на память, содержащую некомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="88db9-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-134">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88db9-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-135">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="88db9-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="88db9-136">Адрес указателя на память, который содержит ошибки создания эффектов, если таковые возникли.</span><span class="sxs-lookup"><span data-stu-id="88db9-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="88db9-137">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88db9-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88db9-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="88db9-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="88db9-139">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="88db9-139">A pointer to the return value.</span></span> <span data-ttu-id="88db9-140">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="88db9-140">May be **NULL**.</span></span> <span data-ttu-id="88db9-141">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="88db9-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88db9-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88db9-142">Return value</span></span>

<span data-ttu-id="88db9-143">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88db9-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88db9-144">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="88db9-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88db9-145">Требования</span><span class="sxs-lookup"><span data-stu-id="88db9-145">Requirements</span></span>



| <span data-ttu-id="88db9-146">Требование</span><span class="sxs-lookup"><span data-stu-id="88db9-146">Requirement</span></span> | <span data-ttu-id="88db9-147">Значение</span><span class="sxs-lookup"><span data-stu-id="88db9-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88db9-148">Header</span><span class="sxs-lookup"><span data-stu-id="88db9-148">Header</span></span><br/>  | <dl> <span data-ttu-id="88db9-149"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="88db9-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="88db9-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88db9-150">Library</span></span><br/> | <dl> <span data-ttu-id="88db9-151"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88db9-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="88db9-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88db9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88db9-153">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="88db9-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

