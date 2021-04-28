---
description: Функция D3DXGetImageInfoFromResource — получение сведений об определенном изображении в ресурсе.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: Функция D3DXGetImageInfoFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114452"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="03fc0-103">Функция D3DXGetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="03fc0-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="03fc0-104">Извлекает сведения об определенном изображении в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="03fc0-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03fc0-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="03fc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03fc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fc0-107">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03fc0-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03fc0-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03fc0-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03fc0-109">Модуль, в котором загружен ресурс.</span><span class="sxs-lookup"><span data-stu-id="03fc0-109">Module where the resource is loaded.</span></span> <span data-ttu-id="03fc0-110">Присвойте этому параметру **значение NULL** , чтобы указать модуль, связанный с образом, который операционная система использовала для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="03fc0-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="03fc0-111">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03fc0-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03fc0-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03fc0-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03fc0-113">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="03fc0-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="03fc0-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="03fc0-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="03fc0-115">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="03fc0-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="03fc0-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="03fc0-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="03fc0-117">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03fc0-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03fc0-118">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="03fc0-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="03fc0-119">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="03fc0-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fc0-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03fc0-120">Return value</span></span>

<span data-ttu-id="03fc0-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03fc0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03fc0-122">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="03fc0-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="03fc0-123">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="03fc0-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="03fc0-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="03fc0-124">Remarks</span></span>

<span data-ttu-id="03fc0-125">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="03fc0-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="03fc0-126">Если определен Юникод, вызов функции разрешается в D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="03fc0-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="03fc0-127">В противном случае вызов функции разрешается в D3DXGetImageInfoFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="03fc0-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="03fc0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="03fc0-128">Requirements</span></span>



| <span data-ttu-id="03fc0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="03fc0-129">Requirement</span></span> | <span data-ttu-id="03fc0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="03fc0-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03fc0-131">Header</span><span class="sxs-lookup"><span data-stu-id="03fc0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="03fc0-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="03fc0-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="03fc0-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03fc0-133">Library</span></span><br/> | <dl> <span data-ttu-id="03fc0-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03fc0-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="03fc0-135">См. также</span><span class="sxs-lookup"><span data-stu-id="03fc0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fc0-136">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="03fc0-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="03fc0-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="03fc0-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="03fc0-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="03fc0-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
