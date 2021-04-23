---
title: Структура D3DX11_IMAGE_INFO (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. | Структура D3DX11_IMAGE_INFO (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO структура Direct3D 11
- Указатель структуры LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987209"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="a5d33-107">\_ \_ Структура сведений об ОБРАЗе D3DX11</span><span class="sxs-lookup"><span data-stu-id="a5d33-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="a5d33-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="a5d33-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="a5d33-109">При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур.</span><span class="sxs-lookup"><span data-stu-id="a5d33-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="a5d33-110">Значение D3DX11 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="a5d33-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d33-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5d33-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="a5d33-112">Участники</span><span class="sxs-lookup"><span data-stu-id="a5d33-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5d33-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="a5d33-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-115">Целевая Ширина текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5d33-115">The target width of the texture.</span></span> <span data-ttu-id="a5d33-116">Если фактическая ширина текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую ширину.</span><span class="sxs-lookup"><span data-stu-id="a5d33-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="a5d33-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-119">Целевая Высота текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5d33-119">The target height of the texture.</span></span> <span data-ttu-id="a5d33-120">Если фактическая высота текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую высоту.</span><span class="sxs-lookup"><span data-stu-id="a5d33-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-121">**Depth**</span><span class="sxs-lookup"><span data-stu-id="a5d33-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-122">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-123">Глубина текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5d33-123">The depth of the texture.</span></span> <span data-ttu-id="a5d33-124">Это относится только к текстурам томов.</span><span class="sxs-lookup"><span data-stu-id="a5d33-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-125">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="a5d33-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-126">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-127">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="a5d33-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-128">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="a5d33-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-129">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-130">Максимальное число уровней mipmap в текстуре.</span><span class="sxs-lookup"><span data-stu-id="a5d33-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="a5d33-131">См. примечания в разделе [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="a5d33-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="a5d33-132">Использование значения 0 или D3DX11 \_ по умолчанию приведет к созданию всей цепочки mipmap.</span><span class="sxs-lookup"><span data-stu-id="a5d33-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-133">**мискфлагс**</span><span class="sxs-lookup"><span data-stu-id="a5d33-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-134">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-135">Различные свойства ресурсов, заданные с помощью флага [**D3D11 \_ ресурса " \_ \_ Прочие**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ".</span><span class="sxs-lookup"><span data-stu-id="a5d33-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-136">**Формат**</span><span class="sxs-lookup"><span data-stu-id="a5d33-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-137">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-138">Перечисление [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , определяющее формат, в котором текстура будет находиться после загрузки.</span><span class="sxs-lookup"><span data-stu-id="a5d33-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-139">**ресаурцедименсион**</span><span class="sxs-lookup"><span data-stu-id="a5d33-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-140">Тип: **[ **D3D11 \_ ресурс \_ измерение**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-141">Значение [**\_ \_ измерения ресурса D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , которое определяет тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="a5d33-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="a5d33-142">**имажефилеформат**</span><span class="sxs-lookup"><span data-stu-id="a5d33-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a5d33-143">Тип: **[ **D3DX11 \_ image \_ File \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="a5d33-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5d33-144">Значение [**\_ \_ \_ формата файла изображения D3DX11**](d3dx11-image-file-format.md) , определяющее формат изображения.</span><span class="sxs-lookup"><span data-stu-id="a5d33-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5d33-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5d33-145">Remarks</span></span>

<span data-ttu-id="a5d33-146">Эта структура используется такими методами, как: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)или [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="a5d33-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d33-147">Требования</span><span class="sxs-lookup"><span data-stu-id="a5d33-147">Requirements</span></span>



| <span data-ttu-id="a5d33-148">Требование</span><span class="sxs-lookup"><span data-stu-id="a5d33-148">Requirement</span></span> | <span data-ttu-id="a5d33-149">Значение</span><span class="sxs-lookup"><span data-stu-id="a5d33-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d33-150">Header</span><span class="sxs-lookup"><span data-stu-id="a5d33-150">Header</span></span><br/> | <dl> <span data-ttu-id="a5d33-151"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d33-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d33-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5d33-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d33-153">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="a5d33-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

