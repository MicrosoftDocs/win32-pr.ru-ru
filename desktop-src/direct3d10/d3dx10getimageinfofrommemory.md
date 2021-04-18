---
description: Получение сведений о изображении, которое уже загружено в память.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: Функция D3DX10GetImageInfoFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713713"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="0a2f7-103">Функция D3DX10GetImageInfoFromMemory</span><span class="sxs-lookup"><span data-stu-id="0a2f7-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="0a2f7-104">Получение сведений о изображении, которое уже загружено в память.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a2f7-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0a2f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a2f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a2f7-107">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2f7-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2f7-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2f7-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a2f7-109">Указатель на изображение в памяти.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0a2f7-110">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2f7-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2f7-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2f7-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a2f7-112">Размер изображения в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0a2f7-113">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2f7-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2f7-114">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a2f7-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0a2f7-115">Дополнительный конвейер потока, который можно использовать для асинхронной загрузки информации.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="0a2f7-116">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-116">Can be **NULL**.</span></span> <span data-ttu-id="0a2f7-117">См. [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0a2f7-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a2f7-118">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2f7-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2f7-119">Тип: **[ **\_ \_ сведения об образе D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a2f7-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="0a2f7-120">Сведения о изображении в памяти.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0a2f7-121">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a2f7-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2f7-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0a2f7-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0a2f7-123">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-123">A pointer to the return value.</span></span> <span data-ttu-id="0a2f7-124">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-124">May be **NULL**.</span></span> <span data-ttu-id="0a2f7-125">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="0a2f7-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a2f7-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a2f7-126">Return value</span></span>

<span data-ttu-id="0a2f7-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a2f7-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a2f7-128">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0a2f7-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a2f7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0a2f7-129">Requirements</span></span>



| <span data-ttu-id="0a2f7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0a2f7-130">Requirement</span></span> | <span data-ttu-id="0a2f7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0a2f7-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2f7-132">Header</span><span class="sxs-lookup"><span data-stu-id="0a2f7-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0a2f7-133"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a2f7-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0a2f7-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a2f7-134">Library</span></span><br/> | <dl> <span data-ttu-id="0a2f7-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a2f7-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0a2f7-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a2f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2f7-137">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0a2f7-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
