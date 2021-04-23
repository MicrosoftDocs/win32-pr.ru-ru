---
description: Инкапсулирует объект сетки в иерархии фрейма преобразования.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Структура D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354180"
---
# <a name="d3dxmeshcontainer-structure"></a><span data-ttu-id="c9db4-103">Структура D3DXMESHCONTAINER</span><span class="sxs-lookup"><span data-stu-id="c9db4-103">D3DXMESHCONTAINER structure</span></span>

<span data-ttu-id="c9db4-104">Инкапсулирует объект сетки в иерархии фрейма преобразования.</span><span class="sxs-lookup"><span data-stu-id="c9db4-104">Encapsulates a mesh object in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9db4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9db4-105">Syntax</span></span>


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a><span data-ttu-id="c9db4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c9db4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9db4-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="c9db4-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-108">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="c9db4-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-109">Имя сетки.</span><span class="sxs-lookup"><span data-stu-id="c9db4-109">Mesh name.</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-110">**мешдата**</span><span class="sxs-lookup"><span data-stu-id="c9db4-110">**MeshData**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-111">Тип: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**</span><span class="sxs-lookup"><span data-stu-id="c9db4-111">Type: **[**D3DXMESHDATA**](d3dxmeshdata.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-112">Тип данных в сетке.</span><span class="sxs-lookup"><span data-stu-id="c9db4-112">Type of data in the mesh.</span></span> <span data-ttu-id="c9db4-113">См. [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="c9db4-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-114">**пматериалс**</span><span class="sxs-lookup"><span data-stu-id="c9db4-114">**pMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-115">Тип: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**</span><span class="sxs-lookup"><span data-stu-id="c9db4-115">Type: **[**LPD3DXMATERIAL**](d3dxmaterial.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-116">Массив материалов для сетки.</span><span class="sxs-lookup"><span data-stu-id="c9db4-116">Array of mesh materials.</span></span> <span data-ttu-id="c9db4-117">См. [**D3DXMATERIAL**](d3dxmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="c9db4-117">See [**D3DXMATERIAL**](d3dxmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-118">**пеффектс**</span><span class="sxs-lookup"><span data-stu-id="c9db4-118">**pEffects**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-119">Тип: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span><span class="sxs-lookup"><span data-stu-id="c9db4-119">Type: **[**LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-120">Указатель на набор параметров эффектов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9db4-120">Pointer to a set of default effect parameters.</span></span> <span data-ttu-id="c9db4-121">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="c9db4-121">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-122">**нумматериалс**</span><span class="sxs-lookup"><span data-stu-id="c9db4-122">**NumMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9db4-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-124">Число материалов в сетке.</span><span class="sxs-lookup"><span data-stu-id="c9db4-124">Number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-125">**паджаценци**</span><span class="sxs-lookup"><span data-stu-id="c9db4-125">**pAdjacency**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9db4-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-127">Указатель на массив из трех DWORD на треугольник сетки, содержащей сведения о смежности.</span><span class="sxs-lookup"><span data-stu-id="c9db4-127">Pointer to an array of three DWORDs per triangle of the mesh that contains adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-128">**пскининфо**</span><span class="sxs-lookup"><span data-stu-id="c9db4-128">**pSkinInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-129">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="c9db4-129">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-130">Указатель на интерфейс сведений об обложке.</span><span class="sxs-lookup"><span data-stu-id="c9db4-130">Pointer to the skin information interface.</span></span> <span data-ttu-id="c9db4-131">См. [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="c9db4-131">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9db4-132">**пнекстмешконтаинер**</span><span class="sxs-lookup"><span data-stu-id="c9db4-132">**pNextMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="c9db4-133">Тип: \* \* \* \* D3DXMESHCONTAINER **\***</span><span class="sxs-lookup"><span data-stu-id="c9db4-133">Type: \*\*\*\*D3DXMESHCONTAINER **\***</span></span>

</dd> <dd>

<span data-ttu-id="c9db4-134">Указатель на следующий контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="c9db4-134">Pointer to the next mesh container.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9db4-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9db4-135">Remarks</span></span>

<span data-ttu-id="c9db4-136">Приложение может быть производным от этой структуры для добавления других данных.</span><span class="sxs-lookup"><span data-stu-id="c9db4-136">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9db4-137">Требования</span><span class="sxs-lookup"><span data-stu-id="c9db4-137">Requirements</span></span>



| <span data-ttu-id="c9db4-138">Требование</span><span class="sxs-lookup"><span data-stu-id="c9db4-138">Requirement</span></span> | <span data-ttu-id="c9db4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c9db4-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9db4-140">Header</span><span class="sxs-lookup"><span data-stu-id="c9db4-140">Header</span></span><br/> | <dl> <span data-ttu-id="c9db4-141"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9db4-141"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9db4-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9db4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9db4-143">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="c9db4-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
