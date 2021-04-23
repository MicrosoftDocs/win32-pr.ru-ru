---
description: Извлекает сведения о заданном файле изображения.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Функция D3DXGetImageInfoFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff5d540871482b2628fd48deb382121591a9594f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713671"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="b2773-103">Функция D3DXGetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="b2773-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="b2773-104">Извлекает сведения о заданном файле изображения.</span><span class="sxs-lookup"><span data-stu-id="b2773-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2773-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2773-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b2773-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2773-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2773-107">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2773-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2773-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2773-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2773-109">Имя файла образа, сведения о котором нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b2773-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="b2773-110">Если определен Юникод или \_ Unicode, этот параметр имеет тип лпквстр, в противном случае — тип LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b2773-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="b2773-111">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2773-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2773-112">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2773-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="b2773-113">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="b2773-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2773-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2773-114">Return value</span></span>

<span data-ttu-id="b2773-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2773-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2773-116">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b2773-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2773-117">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="b2773-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b2773-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2773-118">Remarks</span></span>

<span data-ttu-id="b2773-119">Эта функция поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="b2773-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2773-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b2773-120">Requirements</span></span>



| <span data-ttu-id="b2773-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b2773-121">Requirement</span></span> | <span data-ttu-id="b2773-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b2773-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2773-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2773-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b2773-124"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2773-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b2773-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2773-125">Library</span></span><br/> | <dl> <span data-ttu-id="b2773-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2773-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b2773-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2773-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2773-128">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b2773-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b2773-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="b2773-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="b2773-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="b2773-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
