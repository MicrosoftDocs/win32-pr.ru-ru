---
description: Извлекает сведения о заданном файле изображения в памяти.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: Функция D3DXGetImageInfoFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713670"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="b68a8-103">Функция D3DXGetImageInfoFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="b68a8-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="b68a8-104">Извлекает сведения о заданном файле изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="b68a8-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b68a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b68a8-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b68a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b68a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b68a8-107">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b68a8-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68a8-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b68a8-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b68a8-109">ПУСТОЙ указатель на исходный файл в памяти.</span><span class="sxs-lookup"><span data-stu-id="b68a8-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="b68a8-110">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b68a8-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68a8-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b68a8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b68a8-112">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="b68a8-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="b68a8-113">.</span><span class="sxs-lookup"><span data-stu-id="b68a8-113">.</span></span>

</dd> <dt>

<span data-ttu-id="b68a8-114">*псрЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b68a8-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68a8-115">Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b68a8-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="b68a8-116">Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="b68a8-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b68a8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b68a8-117">Return value</span></span>

<span data-ttu-id="b68a8-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b68a8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b68a8-119">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b68a8-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b68a8-120">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="b68a8-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="b68a8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b68a8-121">Requirements</span></span>



| <span data-ttu-id="b68a8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b68a8-122">Requirement</span></span> | <span data-ttu-id="b68a8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b68a8-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b68a8-124">Header</span><span class="sxs-lookup"><span data-stu-id="b68a8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b68a8-125"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b68a8-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b68a8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b68a8-126">Library</span></span><br/> | <dl> <span data-ttu-id="b68a8-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b68a8-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b68a8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b68a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68a8-129">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b68a8-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b68a8-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="b68a8-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="b68a8-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="b68a8-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
