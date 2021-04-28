---
description: Структура D3DX10_IMAGE_INFO — Возвращает описание исходного содержимого файла изображения.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Структура D3DX10_IMAGE_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105482"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="b35f7-103">\_ \_ Структура сведений об ОБРАЗе D3DX10</span><span class="sxs-lookup"><span data-stu-id="b35f7-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="b35f7-104">Возвращает описание исходного содержимого файла изображения.</span><span class="sxs-lookup"><span data-stu-id="b35f7-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b35f7-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="b35f7-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b35f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b35f7-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="b35f7-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-109">Ширина исходного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b35f7-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="b35f7-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-112">Высота исходного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b35f7-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-113">**Глубина**</span><span class="sxs-lookup"><span data-stu-id="b35f7-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-115">Глубина исходного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b35f7-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="b35f7-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-118">Размер массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="b35f7-118">Size of the texture array.</span></span> <span data-ttu-id="b35f7-119">*Размера массива* будет иметь значение 1 для одного образа.</span><span class="sxs-lookup"><span data-stu-id="b35f7-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-120">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="b35f7-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-122">Число уровней mipmap в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="b35f7-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-123">**мискфлагс**</span><span class="sxs-lookup"><span data-stu-id="b35f7-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-125">Прочие свойства ресурсов (см. раздел [**D3D10 \_ Resource, \_ \_ флаг**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="b35f7-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-126">**Формат**</span><span class="sxs-lookup"><span data-stu-id="b35f7-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-127">Тип: **[ **\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-128">Значение из перечислимого типа в [**\_ формате DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , которое наиболее точно описывает данные в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="b35f7-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-129">**ресаурцедименсион**</span><span class="sxs-lookup"><span data-stu-id="b35f7-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-130">Тип: **[ **D3D10 \_ ресурс \_ измерение**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-131">Представляет тип текстуры, хранящейся в файле.</span><span class="sxs-lookup"><span data-stu-id="b35f7-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="b35f7-132">См. раздел [**\_ \_ измерение ресурсов D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="b35f7-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="b35f7-133">**имажефилеформат**</span><span class="sxs-lookup"><span data-stu-id="b35f7-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="b35f7-134">Тип: **[ **D3DX10 \_ image \_ File \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="b35f7-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b35f7-135">Представляет формат файла изображения.</span><span class="sxs-lookup"><span data-stu-id="b35f7-135">Represents the format of the image file.</span></span> <span data-ttu-id="b35f7-136">См. раздел [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="b35f7-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b35f7-137">Требования</span><span class="sxs-lookup"><span data-stu-id="b35f7-137">Requirements</span></span>



| <span data-ttu-id="b35f7-138">Требование</span><span class="sxs-lookup"><span data-stu-id="b35f7-138">Requirement</span></span> | <span data-ttu-id="b35f7-139">Значение</span><span class="sxs-lookup"><span data-stu-id="b35f7-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b35f7-140">Header</span><span class="sxs-lookup"><span data-stu-id="b35f7-140">Header</span></span><br/> | <dl> <span data-ttu-id="b35f7-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b35f7-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b35f7-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b35f7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35f7-143">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="b35f7-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
