---
description: Создает сетку обложки из другой сетки.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Функция D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547927"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="469a6-103">Функция D3DXCreateSkinInfoFromBlendedMesh</span><span class="sxs-lookup"><span data-stu-id="469a6-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="469a6-104">Создает сетку обложки из другой сетки.</span><span class="sxs-lookup"><span data-stu-id="469a6-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="469a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="469a6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="469a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="469a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="469a6-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="469a6-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="469a6-108">Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="469a6-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="469a6-109">Указатель на объект [**ID3DXBaseMesh**](id3dxbasemesh.md) — сетку, из которой создается сетка обложки.</span><span class="sxs-lookup"><span data-stu-id="469a6-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="469a6-110">*Нумбонес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="469a6-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="469a6-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="469a6-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="469a6-112">Длина массива, присоединенного к Бонеид.</span><span class="sxs-lookup"><span data-stu-id="469a6-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="469a6-113">См. [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="469a6-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="469a6-114">*пбонекомбинатионтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="469a6-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="469a6-115">Тип: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="469a6-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="469a6-116">Указатель на массив сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="469a6-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="469a6-117">См. [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="469a6-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="469a6-118">*ппскининфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="469a6-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="469a6-119">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="469a6-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="469a6-120">Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий созданный объект сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="469a6-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="469a6-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="469a6-121">Return value</span></span>

<span data-ttu-id="469a6-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="469a6-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="469a6-123">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="469a6-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="469a6-124">Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="469a6-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="469a6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="469a6-125">Requirements</span></span>



| <span data-ttu-id="469a6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="469a6-126">Requirement</span></span> | <span data-ttu-id="469a6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="469a6-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="469a6-128">Header</span><span class="sxs-lookup"><span data-stu-id="469a6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="469a6-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="469a6-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="469a6-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="469a6-130">Library</span></span><br/> | <dl> <span data-ttu-id="469a6-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="469a6-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="469a6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="469a6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469a6-133">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="469a6-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
