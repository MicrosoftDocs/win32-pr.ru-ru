---
description: Возвращает описание исходного содержимого файла изображения.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Структура D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821069"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="3faae-103">\_Структура сведений о D3DXIMAGE</span><span class="sxs-lookup"><span data-stu-id="3faae-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="3faae-104">Возвращает описание исходного содержимого файла изображения.</span><span class="sxs-lookup"><span data-stu-id="3faae-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3faae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3faae-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="3faae-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3faae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3faae-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="3faae-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-109">Ширина исходного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="3faae-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3faae-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="3faae-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-112">Высота исходного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="3faae-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3faae-113">**Depth**</span><span class="sxs-lookup"><span data-stu-id="3faae-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-115">Глубина исходного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="3faae-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3faae-116">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="3faae-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-118">Число уровней MIP в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="3faae-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="3faae-119">**Формат**</span><span class="sxs-lookup"><span data-stu-id="3faae-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-120">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-121">Значение из перечислимого типа [D3DFORMAT](d3dformat.md) , которое наиболее точно описывает данные в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="3faae-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="3faae-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3faae-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-123">Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-124">Представляет тип текстуры, хранящейся в файле.</span><span class="sxs-lookup"><span data-stu-id="3faae-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="3faae-125">Это либо D3DRTYPEная \_ текстура, D3DRTYPE \_ волуметекстуре, либо D3DRTYPE \_ кубетекстуре.</span><span class="sxs-lookup"><span data-stu-id="3faae-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="3faae-126">**имажефилеформат**</span><span class="sxs-lookup"><span data-stu-id="3faae-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="3faae-127">Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3faae-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3faae-128">Представляет формат файла изображения.</span><span class="sxs-lookup"><span data-stu-id="3faae-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3faae-129">Требования</span><span class="sxs-lookup"><span data-stu-id="3faae-129">Requirements</span></span>



| <span data-ttu-id="3faae-130">Требование</span><span class="sxs-lookup"><span data-stu-id="3faae-130">Requirement</span></span> | <span data-ttu-id="3faae-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3faae-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3faae-132">Header</span><span class="sxs-lookup"><span data-stu-id="3faae-132">Header</span></span><br/> | <dl> <span data-ttu-id="3faae-133"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3faae-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3faae-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3faae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3faae-135">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="3faae-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
