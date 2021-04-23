---
title: Функция D3DX11CreateShaderResourceViewFromFile (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать следующие библиотеки Директкстк (Runtime), Креатекскскстекстурефромфиле (где XXX — DDS или WIC) Директкстекс Library (Tools), Лоадфромксксксфиле (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Затем Креатешадерресаурцевиев создайте представление шейдера-ресурса из файла.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- D3DX11CreateShaderResourceViewFromFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355350"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a><span data-ttu-id="f1f35-105">Функция D3DX11CreateShaderResourceViewFromFile</span><span class="sxs-lookup"><span data-stu-id="f1f35-105">D3DX11CreateShaderResourceViewFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="f1f35-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f1f35-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="f1f35-107">Вместо использования этой функции рекомендуется использовать следующие средства:</span><span class="sxs-lookup"><span data-stu-id="f1f35-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="f1f35-108">Библиотека [директкстк](https://github.com/Microsoft/DirectXTK) (Runtime), **КРЕАТЕКСКСКСТЕКСТУРЕФРОМФИЛЕ** (где XXX — DDS или WIC)</span><span class="sxs-lookup"><span data-stu-id="f1f35-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="f1f35-109">Библиотека [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **ЛОАДФРОМКСКСКСФИЛЕ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр), затем **креатешадерресаурцевиев**</span><span class="sxs-lookup"><span data-stu-id="f1f35-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="f1f35-110">Создание представления "шейдер — представление ресурсов" из файла.</span><span class="sxs-lookup"><span data-stu-id="f1f35-110">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f35-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1f35-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="f1f35-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1f35-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f35-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f35-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f35-114">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="f1f35-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="f1f35-115">Указатель на устройство (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), которое будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="f1f35-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f1f35-116">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f35-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f35-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f1f35-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f1f35-118">Имя файла, содержащего представление шейдера-ресурса.</span><span class="sxs-lookup"><span data-stu-id="f1f35-118">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="f1f35-119">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="f1f35-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f1f35-120">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f1f35-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="f1f35-121">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f35-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f35-122">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1f35-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="f1f35-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f1f35-123">Optional.</span></span> <span data-ttu-id="f1f35-124">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="f1f35-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f1f35-125">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f35-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f35-126">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1f35-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="f1f35-127">Указатель на интерфейс генератора потоков (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="f1f35-127">Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="f1f35-128">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="f1f35-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="f1f35-129">*ппшадерресаурцевиев* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1f35-129">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f35-130">Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1f35-130">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="f1f35-131">Адрес указателя на представление шейдера-ресурса (см. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="f1f35-131">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="f1f35-132">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1f35-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f35-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="f1f35-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="f1f35-134">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="f1f35-134">A pointer to the return value.</span></span> <span data-ttu-id="f1f35-135">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f1f35-135">May be **NULL**.</span></span> <span data-ttu-id="f1f35-136">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1f35-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f35-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1f35-137">Return value</span></span>

<span data-ttu-id="f1f35-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1f35-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1f35-139">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f1f35-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f35-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1f35-140">Remarks</span></span>

<span data-ttu-id="f1f35-141">Список поддерживаемых форматов изображений см. в разделе [**\_ \_ \_ Формат файла изображения D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="f1f35-141">For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f35-142">Требования</span><span class="sxs-lookup"><span data-stu-id="f1f35-142">Requirements</span></span>



| <span data-ttu-id="f1f35-143">Требование</span><span class="sxs-lookup"><span data-stu-id="f1f35-143">Requirement</span></span> | <span data-ttu-id="f1f35-144">Значение</span><span class="sxs-lookup"><span data-stu-id="f1f35-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f35-145">Header</span><span class="sxs-lookup"><span data-stu-id="f1f35-145">Header</span></span><br/>  | <dl> <span data-ttu-id="f1f35-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f35-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f1f35-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1f35-147">Library</span></span><br/> | <dl> <span data-ttu-id="f1f35-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1f35-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1f35-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1f35-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f35-150">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="f1f35-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

