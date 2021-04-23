---
description: Создает пустой объект сетки обложки, используя код гибкого формата вершин (ФВФ).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: Функция D3DXCreateSkinInfoFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713696"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="6e183-103">Функция D3DXCreateSkinInfoFVF</span><span class="sxs-lookup"><span data-stu-id="6e183-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="6e183-104">Создает пустой объект сетки обложки, используя код гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="6e183-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e183-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e183-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6e183-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e183-107">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e183-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e183-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e183-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e183-109">Число вершин для сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="6e183-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6e183-110">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e183-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e183-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e183-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e183-112">Сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины для возвращаемой сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="6e183-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6e183-113">*Нумбонес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e183-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e183-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e183-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e183-115">Число костей для сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="6e183-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6e183-116">*ппскининфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6e183-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e183-117">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e183-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="6e183-118">Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий созданный объект сведений о обложке.</span><span class="sxs-lookup"><span data-stu-id="6e183-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e183-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e183-119">Return value</span></span>

<span data-ttu-id="6e183-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e183-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e183-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6e183-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6e183-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6e183-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e183-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e183-123">Remarks</span></span>

<span data-ttu-id="6e183-124">Используйте [**сетбонеинфлуенце**](id3dxskininfo--setboneinfluence.md) для заполнения пустого объекта сетки обложки, возвращаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="6e183-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e183-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6e183-125">Requirements</span></span>



| <span data-ttu-id="6e183-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6e183-126">Requirement</span></span> | <span data-ttu-id="6e183-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6e183-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e183-128">Header</span><span class="sxs-lookup"><span data-stu-id="6e183-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6e183-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e183-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6e183-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6e183-130">Library</span></span><br/> | <dl> <span data-ttu-id="6e183-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e183-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e183-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e183-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e183-133">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="6e183-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6e183-134">**сетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="6e183-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
