---
description: Определяет сведения о положении, текстуре и цвете спрайта.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Структура D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720946"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="0be7b-103">\_Структура D3DX10 спрайта</span><span class="sxs-lookup"><span data-stu-id="0be7b-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="0be7b-104">Определяет сведения о положении, текстуре и цвете спрайта.</span><span class="sxs-lookup"><span data-stu-id="0be7b-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be7b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0be7b-105">Syntax</span></span>


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a><span data-ttu-id="0be7b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0be7b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0be7b-107">**матворлд**</span><span class="sxs-lookup"><span data-stu-id="0be7b-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="0be7b-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="0be7b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0be7b-109">Преобразование модели спрайта в мир.</span><span class="sxs-lookup"><span data-stu-id="0be7b-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="0be7b-110">Определяет положение и ориентацию спрайта в мировом пространстве.</span><span class="sxs-lookup"><span data-stu-id="0be7b-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="0be7b-111">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="0be7b-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="0be7b-112">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="0be7b-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0be7b-113">Смещение от верхнего левого угла текстуры, указывающего, где в текстуре должно начинаться изображение спрайта.</span><span class="sxs-lookup"><span data-stu-id="0be7b-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="0be7b-114">**Текскурд** находится в координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="0be7b-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0be7b-115">**текссизе**</span><span class="sxs-lookup"><span data-stu-id="0be7b-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="0be7b-116">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="0be7b-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0be7b-117">Вектор, содержащий ширину и высоту спрайта в координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="0be7b-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0be7b-118">**колормодулате**</span><span class="sxs-lookup"><span data-stu-id="0be7b-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="0be7b-119">Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="0be7b-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0be7b-120">Цвет, который будет умножен до цвета пикселя перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="0be7b-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="0be7b-121">**птекстуре**</span><span class="sxs-lookup"><span data-stu-id="0be7b-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="0be7b-122">Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="0be7b-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="0be7b-123">Указатель на представление шейдера, представляющее текстуру спрайта.</span><span class="sxs-lookup"><span data-stu-id="0be7b-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="0be7b-124">См. раздел [**интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="0be7b-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="0be7b-125">**текстуреиндекс**</span><span class="sxs-lookup"><span data-stu-id="0be7b-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="0be7b-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0be7b-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0be7b-127">Индекс текстуры.</span><span class="sxs-lookup"><span data-stu-id="0be7b-127">The index of the texture.</span></span> <span data-ttu-id="0be7b-128">Если Птекстуре не представляет массив текстуры, это значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="0be7b-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0be7b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0be7b-129">Requirements</span></span>



| <span data-ttu-id="0be7b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0be7b-130">Requirement</span></span> | <span data-ttu-id="0be7b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0be7b-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0be7b-132">Header</span><span class="sxs-lookup"><span data-stu-id="0be7b-132">Header</span></span><br/> | <dl> <span data-ttu-id="0be7b-133"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be7b-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be7b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0be7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be7b-135">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="0be7b-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
