---
description: Извлекает сведения об определенном изображении в ресурсе.
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Функция D3DX10GetImageInfoFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e77efb973e20a5db708d28b49f0cee27bee7d4e5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273731"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="9d49a-103">Функция D3DX10GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="9d49a-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="9d49a-104">Извлекает сведения об определенном изображении в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="9d49a-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d49a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d49a-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="9d49a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d49a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d49a-107">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d49a-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d49a-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d49a-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d49a-109">Модуль, в котором загружен ресурс.</span><span class="sxs-lookup"><span data-stu-id="9d49a-109">Module where the resource is loaded.</span></span> <span data-ttu-id="9d49a-110">Присвойте этому параметру **значение NULL** , чтобы указать модуль, связанный с образом, который операционная система использовала для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="9d49a-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="9d49a-111">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d49a-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d49a-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d49a-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d49a-113">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="9d49a-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="9d49a-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="9d49a-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9d49a-115">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9d49a-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="9d49a-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="9d49a-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9d49a-117">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d49a-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d49a-118">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d49a-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="9d49a-119">Дополнительный конвейер потока, который можно использовать для асинхронной загрузки информации.</span><span class="sxs-lookup"><span data-stu-id="9d49a-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="9d49a-120">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9d49a-120">Can be **NULL**.</span></span> <span data-ttu-id="9d49a-121">См. [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="9d49a-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d49a-122">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d49a-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d49a-123">Тип: **[ **\_ \_ сведения об образе D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d49a-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="9d49a-124">Указатель на \_ \_ структуру сведений об изображении D3DX10, которая должна быть заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="9d49a-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="9d49a-125">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9d49a-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d49a-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="9d49a-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="9d49a-127">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="9d49a-127">A pointer to the return value.</span></span> <span data-ttu-id="9d49a-128">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9d49a-128">May be **NULL**.</span></span> <span data-ttu-id="9d49a-129">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="9d49a-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d49a-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d49a-130">Return value</span></span>

<span data-ttu-id="9d49a-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d49a-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d49a-132">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9d49a-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9d49a-133">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="9d49a-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="9d49a-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d49a-134">Remarks</span></span>

<span data-ttu-id="9d49a-135">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="9d49a-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9d49a-136">Если определен Юникод, вызов функции разрешается в D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="9d49a-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="9d49a-137">В противном случае вызов функции разрешается в D3DX10GetImageInfoFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="9d49a-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d49a-138">Требования</span><span class="sxs-lookup"><span data-stu-id="9d49a-138">Requirements</span></span>



| <span data-ttu-id="9d49a-139">Требование</span><span class="sxs-lookup"><span data-stu-id="9d49a-139">Requirement</span></span> | <span data-ttu-id="9d49a-140">Значение</span><span class="sxs-lookup"><span data-stu-id="9d49a-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d49a-141">Header</span><span class="sxs-lookup"><span data-stu-id="9d49a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="9d49a-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d49a-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9d49a-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d49a-143">Library</span></span><br/> | <dl> <span data-ttu-id="9d49a-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d49a-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9d49a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d49a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d49a-146">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="9d49a-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
