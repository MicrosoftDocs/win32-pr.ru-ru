---
description: Функция D3DX10GetImageInfoFromFile — получение сведений о заданном файле изображения.
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: Функция D3DX10GetImageInfoFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3e11c4cb52176b0a144e164501f8c70d1e3678c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098340"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="05ac5-103">Функция D3DX10GetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="05ac5-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="05ac5-104">Извлекает сведения о заданном файле изображения.</span><span class="sxs-lookup"><span data-stu-id="05ac5-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ac5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05ac5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="05ac5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05ac5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05ac5-107">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05ac5-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ac5-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05ac5-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05ac5-109">Имя файла образа, сведения о котором нужно получить.</span><span class="sxs-lookup"><span data-stu-id="05ac5-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="05ac5-110">Если определен Юникод или \_ Unicode, этот параметр имеет тип лпквстр, в противном случае — тип LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="05ac5-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="05ac5-111">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05ac5-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ac5-112">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="05ac5-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="05ac5-113">Дополнительный конвейер потока, который можно использовать для асинхронной загрузки информации.</span><span class="sxs-lookup"><span data-stu-id="05ac5-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="05ac5-114">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="05ac5-114">Can be **NULL**.</span></span> <span data-ttu-id="05ac5-115">См. [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="05ac5-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="05ac5-116">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05ac5-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ac5-117">Тип: **[ **\_ \_ сведения об образе D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="05ac5-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="05ac5-118">Указатель на \_ \_ структуру сведений об изображении D3DX10, которая должна быть заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="05ac5-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="05ac5-119">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05ac5-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05ac5-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="05ac5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="05ac5-121">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="05ac5-121">A pointer to the return value.</span></span> <span data-ttu-id="05ac5-122">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="05ac5-122">May be **NULL**.</span></span> <span data-ttu-id="05ac5-123">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="05ac5-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05ac5-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05ac5-124">Return value</span></span>

<span data-ttu-id="05ac5-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05ac5-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05ac5-126">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="05ac5-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="05ac5-127">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="05ac5-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="05ac5-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="05ac5-128">Remarks</span></span>

<span data-ttu-id="05ac5-129">Эта функция поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="05ac5-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="05ac5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="05ac5-130">Requirements</span></span>



| <span data-ttu-id="05ac5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="05ac5-131">Requirement</span></span> | <span data-ttu-id="05ac5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="05ac5-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05ac5-133">Header</span><span class="sxs-lookup"><span data-stu-id="05ac5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="05ac5-134"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="05ac5-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="05ac5-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05ac5-135">Library</span></span><br/> | <dl> <span data-ttu-id="05ac5-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05ac5-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="05ac5-137">См. также</span><span class="sxs-lookup"><span data-stu-id="05ac5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ac5-138">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="05ac5-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
