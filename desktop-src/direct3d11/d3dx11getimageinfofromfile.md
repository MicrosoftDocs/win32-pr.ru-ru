---
title: Функция D3DX11GetImageInfoFromFile (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Жетметадатафромксксксфиле (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Извлекает сведения о заданном файле изображения.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- D3DX11GetImageInfoFromFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081906"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="53cdd-106">Функция D3DX11GetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="53cdd-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="53cdd-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="53cdd-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="53cdd-108">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **ЖЕТМЕТАДАТАФРОМКСКСКСФИЛЕ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр).</span><span class="sxs-lookup"><span data-stu-id="53cdd-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="53cdd-109">Извлекает сведения о заданном файле изображения.</span><span class="sxs-lookup"><span data-stu-id="53cdd-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="53cdd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53cdd-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="53cdd-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="53cdd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53cdd-112">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53cdd-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53cdd-113">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="53cdd-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="53cdd-114">Имя файла образа, сведения о котором нужно получить.</span><span class="sxs-lookup"><span data-stu-id="53cdd-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="53cdd-115">Если определен Юникод или \_ Unicode, этот параметр имеет тип лпквстр, в противном случае — тип LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="53cdd-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="53cdd-116">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53cdd-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53cdd-117">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="53cdd-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="53cdd-118">Дополнительный конвейер потока, который можно использовать для асинхронной загрузки информации.</span><span class="sxs-lookup"><span data-stu-id="53cdd-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="53cdd-119">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="53cdd-119">Can be **NULL**.</span></span> <span data-ttu-id="53cdd-120">См. раздел [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="53cdd-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="53cdd-121">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53cdd-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53cdd-122">Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="53cdd-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="53cdd-123">Указатель на [**\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md) , которые должны быть заполнены описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="53cdd-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="53cdd-124">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53cdd-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53cdd-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="53cdd-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="53cdd-126">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="53cdd-126">A pointer to the return value.</span></span> <span data-ttu-id="53cdd-127">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="53cdd-127">May be **NULL**.</span></span> <span data-ttu-id="53cdd-128">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="53cdd-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53cdd-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53cdd-129">Return value</span></span>

<span data-ttu-id="53cdd-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53cdd-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53cdd-131">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="53cdd-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53cdd-132">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="53cdd-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="53cdd-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="53cdd-133">Remarks</span></span>

<span data-ttu-id="53cdd-134">Эта функция поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="53cdd-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="53cdd-135">Требования</span><span class="sxs-lookup"><span data-stu-id="53cdd-135">Requirements</span></span>



| <span data-ttu-id="53cdd-136">Требование</span><span class="sxs-lookup"><span data-stu-id="53cdd-136">Requirement</span></span> | <span data-ttu-id="53cdd-137">Значение</span><span class="sxs-lookup"><span data-stu-id="53cdd-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53cdd-138">Header</span><span class="sxs-lookup"><span data-stu-id="53cdd-138">Header</span></span><br/>  | <dl> <span data-ttu-id="53cdd-139"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="53cdd-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="53cdd-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53cdd-140">Library</span></span><br/> | <dl> <span data-ttu-id="53cdd-141"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53cdd-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="53cdd-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53cdd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cdd-143">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="53cdd-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

