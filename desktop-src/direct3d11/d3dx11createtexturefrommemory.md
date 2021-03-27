---
title: Функция D3DX11CreateTextureFromMemory (D3DX11. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать следующие библиотеки Директкстк (Runtime), Креатекскскстекстурефроммемори (где XXX — DDS или WIC) Директкстекс Library (Tools), Лоадфромксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Затем Креатетекстуре создает ресурс текстуры из файла, находящегося в системной памяти.
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- D3DX11CreateTextureFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99987e882430da7f5e884f1b22e890947f7105e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000442"
---
# <a name="d3dx11createtexturefrommemory-function"></a><span data-ttu-id="a2cc3-105">Функция D3DX11CreateTextureFromMemory</span><span class="sxs-lookup"><span data-stu-id="a2cc3-105">D3DX11CreateTextureFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="a2cc3-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a2cc3-107">Вместо использования этой функции рекомендуется использовать следующие средства:</span><span class="sxs-lookup"><span data-stu-id="a2cc3-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="a2cc3-108">Библиотека [директкстк](https://github.com/Microsoft/DirectXTK) (Runtime), **КРЕАТЕКСКСКСТЕКСТУРЕФРОММЕМОРИ** (где XXX — DDS или WIC)</span><span class="sxs-lookup"><span data-stu-id="a2cc3-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="a2cc3-109">Библиотека [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **ЛОАДФРОМКСКСКСМЕМОРИ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр), затем **креатетекстуре**</span><span class="sxs-lookup"><span data-stu-id="a2cc3-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="a2cc3-110">Создайте ресурс текстуры из файла, находящегося в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-110">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2cc3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2cc3-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a2cc3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2cc3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2cc3-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-114">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="a2cc3-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="a2cc3-115">Указатель на устройство (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), которое будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a2cc3-116">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-117">Тип: **[ **лпквоид**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a2cc3-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a2cc3-118">Указатель на ресурс в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-118">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="a2cc3-119">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-120">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a2cc3-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a2cc3-121">Размер ресурса в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-121">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="a2cc3-122">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-123">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2cc3-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="a2cc3-124">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-124">Optional.</span></span> <span data-ttu-id="a2cc3-125">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a2cc3-126">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-127">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2cc3-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="a2cc3-128">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a2cc3-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="a2cc3-129">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="a2cc3-130">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-130">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-131">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="a2cc3-131">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="a2cc3-132">Адрес указателя на созданный ресурс.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-132">Address of a pointer to the created resource.</span></span> <span data-ttu-id="a2cc3-133">См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="a2cc3-133">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="a2cc3-134">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a2cc3-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cc3-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a2cc3-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a2cc3-136">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-136">A pointer to the return value.</span></span> <span data-ttu-id="a2cc3-137">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-137">May be **NULL**.</span></span> <span data-ttu-id="a2cc3-138">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="a2cc3-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2cc3-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2cc3-139">Return value</span></span>

<span data-ttu-id="a2cc3-140">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2cc3-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2cc3-141">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a2cc3-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2cc3-142">Требования</span><span class="sxs-lookup"><span data-stu-id="a2cc3-142">Requirements</span></span>



| <span data-ttu-id="a2cc3-143">Требование</span><span class="sxs-lookup"><span data-stu-id="a2cc3-143">Requirement</span></span> | <span data-ttu-id="a2cc3-144">Значение</span><span class="sxs-lookup"><span data-stu-id="a2cc3-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2cc3-145">Header</span><span class="sxs-lookup"><span data-stu-id="a2cc3-145">Header</span></span><br/>  | <dl> <span data-ttu-id="a2cc3-146"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc3-146"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2cc3-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2cc3-147">Library</span></span><br/> | <dl> <span data-ttu-id="a2cc3-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc3-148"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2cc3-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2cc3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2cc3-150">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="a2cc3-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

