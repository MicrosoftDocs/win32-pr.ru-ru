---
title: Функция D3DX11CreateTextureFromResource (D3DX11. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать функции ресурсов, а затем такие библиотеки Директкстк (Runtime), Креатекскскстекстурефроммемори (где XXX — DDS или WIC) Директкстекс Library (Tools), Лоадфромксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр). Затем Креатетекстуре создает текстуру из другого ресурса.
ms.assetid: 2b62239a-c19b-4d4f-9fd2-afcd87ba0fac
keywords:
- D3DX11CreateTextureFromResource функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bea89fe4f8bf6632ada9461b048195335c72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273892"
---
# <a name="d3dx11createtexturefromresource-function"></a><span data-ttu-id="91df2-105">Функция D3DX11CreateTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="91df2-105">D3DX11CreateTextureFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="91df2-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="91df2-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="91df2-107">Вместо использования этой функции рекомендуется использовать [функции ресурсов](/windows/desktop/menurc/resources-functions), а затем:</span><span class="sxs-lookup"><span data-stu-id="91df2-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="91df2-108">Библиотека [директкстк](https://github.com/Microsoft/DirectXTK) (Runtime), **КРЕАТЕКСКСКСТЕКСТУРЕФРОММЕМОРИ** (где XXX — DDS или WIC)</span><span class="sxs-lookup"><span data-stu-id="91df2-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="91df2-109">Библиотека [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **ЛОАДФРОМКСКСКСМЕМОРИ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр), затем **креатетекстуре**</span><span class="sxs-lookup"><span data-stu-id="91df2-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="91df2-110">Создание текстуры из другого ресурса.</span><span class="sxs-lookup"><span data-stu-id="91df2-110">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="91df2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91df2-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromResource(
  _In_  ID3D11Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="91df2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="91df2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91df2-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91df2-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-114">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="91df2-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="91df2-115">Указатель на устройство (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), которое будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="91df2-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="91df2-116">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91df2-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-117">Тип: **[ **хмодуле**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="91df2-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="91df2-118">Маркер исходного ресурса.</span><span class="sxs-lookup"><span data-stu-id="91df2-118">A handle to the source resource.</span></span> <span data-ttu-id="91df2-119">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="91df2-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="91df2-120">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91df2-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-121">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="91df2-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="91df2-122">Строка, содержащая имя исходного ресурса.</span><span class="sxs-lookup"><span data-stu-id="91df2-122">A string that contains the name of the source resource.</span></span> <span data-ttu-id="91df2-123">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="91df2-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="91df2-124">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="91df2-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="91df2-125">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91df2-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-126">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="91df2-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="91df2-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="91df2-127">Optional.</span></span> <span data-ttu-id="91df2-128">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="91df2-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="91df2-129">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91df2-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-130">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="91df2-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="91df2-131">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="91df2-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="91df2-132">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="91df2-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="91df2-133">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91df2-133">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-134">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="91df2-134">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="91df2-135">Адрес указателя на ресурс текстуры (см. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span><span class="sxs-lookup"><span data-stu-id="91df2-135">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="91df2-136">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91df2-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91df2-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="91df2-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="91df2-138">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="91df2-138">A pointer to the return value.</span></span> <span data-ttu-id="91df2-139">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="91df2-139">May be **NULL**.</span></span> <span data-ttu-id="91df2-140">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="91df2-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91df2-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91df2-141">Return value</span></span>

<span data-ttu-id="91df2-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91df2-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91df2-143">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="91df2-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91df2-144">Требования</span><span class="sxs-lookup"><span data-stu-id="91df2-144">Requirements</span></span>



| <span data-ttu-id="91df2-145">Требование</span><span class="sxs-lookup"><span data-stu-id="91df2-145">Requirement</span></span> | <span data-ttu-id="91df2-146">Значение</span><span class="sxs-lookup"><span data-stu-id="91df2-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91df2-147">Header</span><span class="sxs-lookup"><span data-stu-id="91df2-147">Header</span></span><br/>  | <dl> <span data-ttu-id="91df2-148"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="91df2-148"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="91df2-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91df2-149">Library</span></span><br/> | <dl> <span data-ttu-id="91df2-150"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91df2-150"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91df2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91df2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91df2-152">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="91df2-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

