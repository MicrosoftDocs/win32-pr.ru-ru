---
title: Функция D3DX11PreprocessShaderFromFile (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать API D3DPreprocess. Создание шейдера из файла без его компиляции.
ms.assetid: aab08efd-b6b0-44e5-bd68-f32c242d9e94
keywords:
- D3DX11PreprocessShaderFromFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1987ef25688e83a48059805f79af4dc8a88c1ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986993"
---
# <a name="d3dx11preprocessshaderfromfile-function"></a><span data-ttu-id="5eb2a-106">Функция D3DX11PreprocessShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="5eb2a-106">D3DX11PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="5eb2a-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="5eb2a-108">Вместо использования этой функции рекомендуется использовать API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="5eb2a-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="5eb2a-109">Создание шейдера из файла без его компиляции.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-109">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb2a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5eb2a-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="5eb2a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5eb2a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb2a-112">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-113">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5eb2a-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5eb2a-114">Имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-114">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2a-115">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-116">Тип: **const D3D11ный \_ \_ макрос \* шейдера**</span><span class="sxs-lookup"><span data-stu-id="5eb2a-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="5eb2a-117">Массив макросов шейдеров, заканчивающийся нулем; Установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2a-118">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-119">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="5eb2a-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="5eb2a-120">Указатель на интерфейс include; Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2a-121">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-121">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-122">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="5eb2a-122">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="5eb2a-123">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="5eb2a-123">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="5eb2a-124">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-124">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2a-125">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-126">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="5eb2a-126">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="5eb2a-127">Указатель на память, содержащую некомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-127">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2a-128">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-129">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="5eb2a-129">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="5eb2a-130">Адрес указателя на память, который содержит ошибки создания эффектов, если таковые возникли.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-130">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2a-131">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5eb2a-131">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb2a-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="5eb2a-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="5eb2a-133">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-133">A pointer to the return value.</span></span> <span data-ttu-id="5eb2a-134">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-134">May be **NULL**.</span></span> <span data-ttu-id="5eb2a-135">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="5eb2a-135">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb2a-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5eb2a-136">Return value</span></span>

<span data-ttu-id="5eb2a-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5eb2a-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5eb2a-138">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5eb2a-138">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb2a-139">Требования</span><span class="sxs-lookup"><span data-stu-id="5eb2a-139">Requirements</span></span>



| <span data-ttu-id="5eb2a-140">Требование</span><span class="sxs-lookup"><span data-stu-id="5eb2a-140">Requirement</span></span> | <span data-ttu-id="5eb2a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="5eb2a-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb2a-142">Header</span><span class="sxs-lookup"><span data-stu-id="5eb2a-142">Header</span></span><br/>  | <dl> <span data-ttu-id="5eb2a-143"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb2a-143"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="5eb2a-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5eb2a-144">Library</span></span><br/> | <dl> <span data-ttu-id="5eb2a-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5eb2a-145"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5eb2a-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5eb2a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb2a-147">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="5eb2a-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

