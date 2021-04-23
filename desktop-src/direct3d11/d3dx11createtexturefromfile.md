---
title: Функция D3DX11CreateTextureFromFile (D3DX11. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать следующие библиотеки Директкстк (Runtime), Креатекскскстекстурефромфиле (где XXX — DDS или WIC) Директкстекс Library (Tools), Лоадфромксксксфиле (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Затем Креатетекстуре создает ресурс текстуры из файла.
ms.assetid: a84ea166-2296-48d9-a028-b65fd68f2371
keywords:
- D3DX11CreateTextureFromFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ab9bedcfe44238938e47ccb402738d2694b061
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998516"
---
# <a name="d3dx11createtexturefromfile-function"></a><span data-ttu-id="d6cac-105">Функция D3DX11CreateTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="d6cac-105">D3DX11CreateTextureFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="d6cac-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="d6cac-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="d6cac-107">Вместо использования этой функции рекомендуется использовать следующие средства:</span><span class="sxs-lookup"><span data-stu-id="d6cac-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="d6cac-108">Библиотека [директкстк](https://github.com/Microsoft/DirectXTK) (Runtime), **КРЕАТЕКСКСКСТЕКСТУРЕФРОМФИЛЕ** (где XXX — DDS или WIC)</span><span class="sxs-lookup"><span data-stu-id="d6cac-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="d6cac-109">Библиотека [директкстекс](https://github.com/Microsoft/DirectXTex) (Tools), **ЛОАДФРОМКСКСКСФИЛЕ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного изображения для игр), затем **креатетекстуре**</span><span class="sxs-lookup"><span data-stu-id="d6cac-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="d6cac-110">Создание ресурса текстуры из файла.</span><span class="sxs-lookup"><span data-stu-id="d6cac-110">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6cac-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6cac-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromFile(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="d6cac-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6cac-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6cac-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6cac-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cac-114">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="d6cac-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="d6cac-115">Указатель на устройство (см. [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), которое будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="d6cac-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d6cac-116">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6cac-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cac-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6cac-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d6cac-118">Имя файла, содержащего ресурс.</span><span class="sxs-lookup"><span data-stu-id="d6cac-118">The name of the file containing the resource.</span></span> <span data-ttu-id="d6cac-119">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="d6cac-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d6cac-120">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d6cac-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="d6cac-121">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6cac-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cac-122">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6cac-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="d6cac-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d6cac-123">Optional.</span></span> <span data-ttu-id="d6cac-124">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX11**](d3dx11-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="d6cac-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d6cac-125">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6cac-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cac-126">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6cac-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="d6cac-127">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d6cac-127">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="d6cac-128">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="d6cac-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="d6cac-129">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6cac-129">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cac-130">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="d6cac-130">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="d6cac-131">Адрес указателя на ресурс текстуры (см. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span><span class="sxs-lookup"><span data-stu-id="d6cac-131">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="d6cac-132">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6cac-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cac-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d6cac-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d6cac-134">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="d6cac-134">A pointer to the return value.</span></span> <span data-ttu-id="d6cac-135">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d6cac-135">May be **NULL**.</span></span> <span data-ttu-id="d6cac-136">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="d6cac-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6cac-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6cac-137">Return value</span></span>

<span data-ttu-id="d6cac-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6cac-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6cac-139">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d6cac-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6cac-140">Требования</span><span class="sxs-lookup"><span data-stu-id="d6cac-140">Requirements</span></span>



| <span data-ttu-id="d6cac-141">Требование</span><span class="sxs-lookup"><span data-stu-id="d6cac-141">Requirement</span></span> | <span data-ttu-id="d6cac-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d6cac-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6cac-143">Header</span><span class="sxs-lookup"><span data-stu-id="d6cac-143">Header</span></span><br/>  | <dl> <span data-ttu-id="d6cac-144"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6cac-144"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6cac-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6cac-145">Library</span></span><br/> | <dl> <span data-ttu-id="d6cac-146"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6cac-146"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6cac-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6cac-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6cac-148">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="d6cac-148">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

