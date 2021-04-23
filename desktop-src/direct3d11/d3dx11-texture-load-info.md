---
title: Структура D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Описывает параметры, используемые для загрузки текстуры из другой текстуры.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998573"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="f3827-105">\_ \_ \_ Структура сведений о загрузке текстуры D3DX11</span><span class="sxs-lookup"><span data-stu-id="f3827-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="f3827-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f3827-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f3827-107">Описывает параметры, используемые для загрузки текстуры из другой текстуры.</span><span class="sxs-lookup"><span data-stu-id="f3827-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3827-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3827-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="f3827-109">Участники</span><span class="sxs-lookup"><span data-stu-id="f3827-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3827-110">**псркбокс**</span><span class="sxs-lookup"><span data-stu-id="f3827-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-111">Тип: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="f3827-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="f3827-112">Поле текстуры источника (см [**. \_ поле D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="f3827-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="f3827-113">**пдстбокс**</span><span class="sxs-lookup"><span data-stu-id="f3827-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-114">Тип: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="f3827-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="f3827-115">Поле текстуры назначения (см [**. \_ поле D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="f3827-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="f3827-116">**сркфирстмип**</span><span class="sxs-lookup"><span data-stu-id="f3827-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-118">Исходный текстурный уровень mipmap, см. раздел [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="f3827-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="f3827-119">**дстфирстмип**</span><span class="sxs-lookup"><span data-stu-id="f3827-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-120">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-121">Целевая текстура mipmap уровень. Дополнительные сведения см. в разделе [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="f3827-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="f3827-122">**нуммипс**</span><span class="sxs-lookup"><span data-stu-id="f3827-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-123">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-124">Число уровней mipmap в исходной текстуре.</span><span class="sxs-lookup"><span data-stu-id="f3827-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="f3827-125">**сркфирстелемент**</span><span class="sxs-lookup"><span data-stu-id="f3827-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-126">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-127">Первый элемент текстуры источника.</span><span class="sxs-lookup"><span data-stu-id="f3827-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="f3827-128">**дстфирстелемент**</span><span class="sxs-lookup"><span data-stu-id="f3827-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-129">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-130">Первый элемент текстуры назначения.</span><span class="sxs-lookup"><span data-stu-id="f3827-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="f3827-131">**нумелементс**</span><span class="sxs-lookup"><span data-stu-id="f3827-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-132">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-133">Число загружаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="f3827-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="f3827-134">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="f3827-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-135">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-136">Параметры фильтрации при интерполяции (см [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="f3827-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f3827-137">**мипфилтер**</span><span class="sxs-lookup"><span data-stu-id="f3827-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="f3827-138">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3827-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f3827-139">Параметры фильтрации при создании MIP уровней (см [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="f3827-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3827-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3827-140">Remarks</span></span>

<span data-ttu-id="f3827-141">Эта структура используется в вызове [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="f3827-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="f3827-142">Значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="f3827-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="f3827-143">Требования</span><span class="sxs-lookup"><span data-stu-id="f3827-143">Requirements</span></span>



| <span data-ttu-id="f3827-144">Требование</span><span class="sxs-lookup"><span data-stu-id="f3827-144">Requirement</span></span> | <span data-ttu-id="f3827-145">Значение</span><span class="sxs-lookup"><span data-stu-id="f3827-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3827-146">Header</span><span class="sxs-lookup"><span data-stu-id="f3827-146">Header</span></span><br/> | <dl> <span data-ttu-id="f3827-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3827-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3827-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3827-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3827-149">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="f3827-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

