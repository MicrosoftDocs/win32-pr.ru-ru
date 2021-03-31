---
description: Извлекает сведения об определенном изображении в ресурсе.
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
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821077"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="da70c-103">Функция D3DXGetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="da70c-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="da70c-104">Извлекает сведения об определенном изображении в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="da70c-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="da70c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da70c-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="da70c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da70c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da70c-107">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da70c-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70c-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da70c-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da70c-109">Модуль, в котором загружен ресурс.</span><span class="sxs-lookup"><span data-stu-id="da70c-109">Module where the resource is loaded.</span></span> <span data-ttu-id="da70c-110">Присвойте этому параметру **значение NULL** , чтобы указать модуль, связанный с образом, который операционная система использовала для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="da70c-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="da70c-111">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da70c-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70c-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da70c-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da70c-113">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="da70c-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="da70c-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="da70c-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="da70c-115">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="da70c-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="da70c-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="da70c-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da70c-117">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da70c-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70c-118">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="da70c-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="da70c-119">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="da70c-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da70c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da70c-120">Return value</span></span>

<span data-ttu-id="da70c-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da70c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da70c-122">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="da70c-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da70c-123">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="da70c-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="da70c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da70c-124">Remarks</span></span>

<span data-ttu-id="da70c-125">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="da70c-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="da70c-126">Если определен Юникод, вызов функции разрешается в D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="da70c-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="da70c-127">В противном случае вызов функции разрешается в D3DXGetImageInfoFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="da70c-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="da70c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="da70c-128">Requirements</span></span>



| <span data-ttu-id="da70c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="da70c-129">Requirement</span></span> | <span data-ttu-id="da70c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="da70c-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da70c-131">Header</span><span class="sxs-lookup"><span data-stu-id="da70c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="da70c-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="da70c-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="da70c-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da70c-133">Library</span></span><br/> | <dl> <span data-ttu-id="da70c-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da70c-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="da70c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da70c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da70c-136">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="da70c-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="da70c-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="da70c-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="da70c-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="da70c-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
