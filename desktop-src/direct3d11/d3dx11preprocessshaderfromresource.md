---
title: Функция D3DX11PreprocessShaderFromResource (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать API D3DPreprocess. Создание шейдера из ресурса без его компиляции.
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- D3DX11PreprocessShaderFromResource функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998501"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a><span data-ttu-id="4c943-106">Функция D3DX11PreprocessShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="4c943-106">D3DX11PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="4c943-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="4c943-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c943-108">Вместо использования этой функции рекомендуется использовать API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="4c943-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="4c943-109">Создание шейдера из ресурса без его компиляции.</span><span class="sxs-lookup"><span data-stu-id="4c943-109">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c943-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c943-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4c943-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c943-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c943-112">*хмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c943-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-113">Тип: **[ **хмодуле**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c943-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c943-114">Обработчик для модуля ресурсов, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="4c943-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="4c943-115">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="4c943-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="4c943-116">*пресаурценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c943-116">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c943-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c943-118">Имя ресурса в Side Хмодуле, содержащего шейдер.</span><span class="sxs-lookup"><span data-stu-id="4c943-118">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="4c943-119">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="4c943-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4c943-120">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4c943-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-121">*псркфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c943-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-122">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c943-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c943-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="4c943-123">Optional.</span></span> <span data-ttu-id="4c943-124">Имя файла эффектов, которое используется только для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="4c943-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="4c943-125">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4c943-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-126">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c943-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-127">Тип: **const D3D11ный \_ \_ макрос \* шейдера**</span><span class="sxs-lookup"><span data-stu-id="4c943-127">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="4c943-128">Массив макросов шейдеров, заканчивающийся нулем; Установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="4c943-128">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-129">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c943-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-130">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4c943-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="4c943-131">Указатель на интерфейс include; Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="4c943-131">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-132">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c943-132">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-133">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c943-133">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="4c943-134">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="4c943-134">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="4c943-135">Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="4c943-135">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-136">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4c943-136">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-137">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c943-137">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4c943-138">Указатель на память, содержащую некомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="4c943-138">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-139">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4c943-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-140">Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c943-140">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="4c943-141">Адрес указателя на память, который содержит ошибки создания эффектов, если таковые возникли.</span><span class="sxs-lookup"><span data-stu-id="4c943-141">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4c943-142">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4c943-142">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c943-143">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4c943-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4c943-144">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="4c943-144">A pointer to the return value.</span></span> <span data-ttu-id="4c943-145">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4c943-145">May be **NULL**.</span></span> <span data-ttu-id="4c943-146">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="4c943-146">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c943-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c943-147">Return value</span></span>

<span data-ttu-id="4c943-148">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c943-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c943-149">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4c943-149">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c943-150">Требования</span><span class="sxs-lookup"><span data-stu-id="4c943-150">Requirements</span></span>



| <span data-ttu-id="4c943-151">Требование</span><span class="sxs-lookup"><span data-stu-id="4c943-151">Requirement</span></span> | <span data-ttu-id="4c943-152">Значение</span><span class="sxs-lookup"><span data-stu-id="4c943-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c943-153">Header</span><span class="sxs-lookup"><span data-stu-id="4c943-153">Header</span></span><br/>  | <dl> <span data-ttu-id="4c943-154"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c943-154"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="4c943-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c943-155">Library</span></span><br/> | <dl> <span data-ttu-id="4c943-156"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c943-156"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4c943-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c943-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c943-158">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="4c943-158">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

