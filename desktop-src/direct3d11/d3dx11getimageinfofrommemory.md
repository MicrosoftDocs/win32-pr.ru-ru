---
title: Функция D3DX11GetImageInfoFromMemory (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Жетметадатафромксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Получение сведений о изображении, которое уже загружено в память.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- D3DX11GetImageInfoFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986999"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="846ea-106">Функция D3DX11GetImageInfoFromMemory</span><span class="sxs-lookup"><span data-stu-id="846ea-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="846ea-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="846ea-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="846ea-108">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **ЖЕТМЕТАДАТАФРОМКСКСКСМЕМОРИ** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр).</span><span class="sxs-lookup"><span data-stu-id="846ea-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="846ea-109">Получение сведений о изображении, которое уже загружено в память.</span><span class="sxs-lookup"><span data-stu-id="846ea-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="846ea-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="846ea-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="846ea-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="846ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846ea-112">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="846ea-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846ea-113">Тип: **[ **лпквоид**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="846ea-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="846ea-114">Указатель на изображение в памяти.</span><span class="sxs-lookup"><span data-stu-id="846ea-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="846ea-115">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="846ea-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846ea-116">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="846ea-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="846ea-117">Размер изображения в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="846ea-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="846ea-118">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="846ea-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846ea-119">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="846ea-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="846ea-120">Дополнительный конвейер потока, который можно использовать для асинхронной загрузки информации.</span><span class="sxs-lookup"><span data-stu-id="846ea-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="846ea-121">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="846ea-121">Can be **NULL**.</span></span> <span data-ttu-id="846ea-122">См. раздел [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="846ea-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="846ea-123">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="846ea-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846ea-124">Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="846ea-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="846ea-125">Сведения о изображении в памяти.</span><span class="sxs-lookup"><span data-stu-id="846ea-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="846ea-126">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="846ea-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="846ea-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="846ea-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="846ea-128">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="846ea-128">A pointer to the return value.</span></span> <span data-ttu-id="846ea-129">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="846ea-129">May be **NULL**.</span></span> <span data-ttu-id="846ea-130">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="846ea-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846ea-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="846ea-131">Return value</span></span>

<span data-ttu-id="846ea-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="846ea-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="846ea-133">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="846ea-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="846ea-134">Требования</span><span class="sxs-lookup"><span data-stu-id="846ea-134">Requirements</span></span>



| <span data-ttu-id="846ea-135">Требование</span><span class="sxs-lookup"><span data-stu-id="846ea-135">Requirement</span></span> | <span data-ttu-id="846ea-136">Значение</span><span class="sxs-lookup"><span data-stu-id="846ea-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="846ea-137">Header</span><span class="sxs-lookup"><span data-stu-id="846ea-137">Header</span></span><br/>  | <dl> <span data-ttu-id="846ea-138"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="846ea-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="846ea-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="846ea-139">Library</span></span><br/> | <dl> <span data-ttu-id="846ea-140"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="846ea-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="846ea-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="846ea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846ea-142">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="846ea-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

