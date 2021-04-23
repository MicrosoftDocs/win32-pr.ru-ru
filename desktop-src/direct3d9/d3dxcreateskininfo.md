---
description: Создает пустой объект сетки обложки с помощью декларатора.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Функция D3DXCreateSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83ee214eb997414e113256060dbe59d3cd47d1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914728"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="3eed8-103">Функция D3DXCreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3eed8-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="3eed8-104">Создает пустой объект сетки обложки с помощью декларатора.</span><span class="sxs-lookup"><span data-stu-id="3eed8-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eed8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3eed8-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3eed8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3eed8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eed8-107">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eed8-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eed8-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eed8-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3eed8-109">Число вершин для сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="3eed8-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3eed8-110">*пдекларатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eed8-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eed8-111">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="3eed8-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="3eed8-112">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершины для возвращенной сетки.</span><span class="sxs-lookup"><span data-stu-id="3eed8-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3eed8-113">*Нумбонес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eed8-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eed8-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eed8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3eed8-115">Число костей для сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="3eed8-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3eed8-116">*ппскининфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3eed8-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3eed8-117">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="3eed8-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="3eed8-118">Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий созданный объект сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="3eed8-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eed8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3eed8-119">Return value</span></span>

<span data-ttu-id="3eed8-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3eed8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3eed8-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3eed8-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3eed8-122">Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3eed8-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eed8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3eed8-123">Remarks</span></span>

<span data-ttu-id="3eed8-124">Используйте [**сетбонеинфлуенце**](id3dxskininfo--setboneinfluence.md) для заполнения пустого объекта сетки обложки, возвращаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="3eed8-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eed8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3eed8-125">Requirements</span></span>



| <span data-ttu-id="3eed8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3eed8-126">Requirement</span></span> | <span data-ttu-id="3eed8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3eed8-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eed8-128">Header</span><span class="sxs-lookup"><span data-stu-id="3eed8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3eed8-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eed8-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3eed8-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3eed8-130">Library</span></span><br/> | <dl> <span data-ttu-id="3eed8-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3eed8-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3eed8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3eed8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eed8-133">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="3eed8-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="3eed8-134">**сетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="3eed8-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
