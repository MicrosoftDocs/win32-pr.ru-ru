---
description: Описывает параметры, используемые для загрузки текстуры из другой текстуры.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Структура D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720917"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="49308-103">\_ \_ \_ Структура сведений о загрузке текстуры D3DX10</span><span class="sxs-lookup"><span data-stu-id="49308-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="49308-104">Описывает параметры, используемые для загрузки текстуры из другой текстуры.</span><span class="sxs-lookup"><span data-stu-id="49308-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="49308-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49308-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="49308-106">Члены</span><span class="sxs-lookup"><span data-stu-id="49308-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="49308-107">**псркбокс**</span><span class="sxs-lookup"><span data-stu-id="49308-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="49308-108">Тип: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="49308-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="49308-109">Поле текстуры источника (см [**. \_ поле D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="49308-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="49308-110">**пдстбокс**</span><span class="sxs-lookup"><span data-stu-id="49308-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="49308-111">Тип: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="49308-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="49308-112">Поле текстуры назначения (см [**. \_ поле D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="49308-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="49308-113">**сркфирстмип**</span><span class="sxs-lookup"><span data-stu-id="49308-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="49308-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-115">Исходный текстурный уровень mipmap, см. раздел [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="49308-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="49308-116">**дстфирстмип**</span><span class="sxs-lookup"><span data-stu-id="49308-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="49308-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-118">Целевая текстура mipmap уровень. Дополнительные сведения см. в разделе [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="49308-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="49308-119">**нуммипс**</span><span class="sxs-lookup"><span data-stu-id="49308-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="49308-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-121">Число уровней mipmap в исходной текстуре.</span><span class="sxs-lookup"><span data-stu-id="49308-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="49308-122">**сркфирстелемент**</span><span class="sxs-lookup"><span data-stu-id="49308-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="49308-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-124">Первый элемент текстуры источника.</span><span class="sxs-lookup"><span data-stu-id="49308-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="49308-125">**дстфирстелемент**</span><span class="sxs-lookup"><span data-stu-id="49308-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="49308-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-127">Первый элемент текстуры назначения.</span><span class="sxs-lookup"><span data-stu-id="49308-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="49308-128">**нумелементс**</span><span class="sxs-lookup"><span data-stu-id="49308-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="49308-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-130">Число загружаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="49308-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="49308-131">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="49308-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="49308-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-133">Параметры фильтрации при интерполяции (см [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="49308-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="49308-134">**мипфилтер**</span><span class="sxs-lookup"><span data-stu-id="49308-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="49308-135">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49308-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49308-136">Параметры фильтрации при создании MIP уровней (см [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="49308-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49308-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49308-137">Remarks</span></span>

<span data-ttu-id="49308-138">Эта структура используется в вызове [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="49308-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49308-139">Требования</span><span class="sxs-lookup"><span data-stu-id="49308-139">Requirements</span></span>



| <span data-ttu-id="49308-140">Требование</span><span class="sxs-lookup"><span data-stu-id="49308-140">Requirement</span></span> | <span data-ttu-id="49308-141">Значение</span><span class="sxs-lookup"><span data-stu-id="49308-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49308-142">Header</span><span class="sxs-lookup"><span data-stu-id="49308-142">Header</span></span><br/> | <dl> <span data-ttu-id="49308-143"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="49308-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49308-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49308-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49308-145">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="49308-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
