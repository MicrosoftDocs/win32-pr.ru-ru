---
title: Структура CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру ресурсов D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Структура CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713975"
---
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="1f938-104">\_Структура ресурсов \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="1f938-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="1f938-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="1f938-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f938-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f938-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a><span data-ttu-id="1f938-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1f938-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f938-108">**CD3DX12 \_ ресурс \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="1f938-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ ресурса \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="1f938-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-110">**явное CD3DX12 \_ ресурса \_ DESC (const D3D12 \_ ресурс \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="1f938-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-111">Создает новый экземпляр \_ ресурса CD3DX12 \_ DESC, инициализированного с содержимым другой структуры [**ресурса D3D12 ( \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) ).</span><span class="sxs-lookup"><span data-stu-id="1f938-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-112">**CD3DX12 \_ Resource \_ DESC ( \_ \_ измерение измерения ресурса D3D12, выравнивание UInt64, ширина UInt64, высота uint, UInt16 депсораррайсизе, UInt16 МИПЛЕВЕЛС, \_ Формат формата DXGI, uint SAMPLECOUNT, uint самплекуалити, D3D12 \_ \_ Макет макета текстуры, \_ \_ Флаги D3D12 ресурсов)**</span><span class="sxs-lookup"><span data-stu-id="1f938-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-113">Создает новый экземпляр \_ ресурса CD3DX12 \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1f938-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="1f938-114">[**D3D12 \_ Измерение \_ измерения ресурса**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="1f938-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="1f938-115">Выравнивание UINT64</span><span class="sxs-lookup"><span data-stu-id="1f938-115">UINT64 alignment</span></span>

<span data-ttu-id="1f938-116">Ширина UINT64</span><span class="sxs-lookup"><span data-stu-id="1f938-116">UINT64 width</span></span>

<span data-ttu-id="1f938-117">Высота UINT</span><span class="sxs-lookup"><span data-stu-id="1f938-117">UINT height</span></span>

<span data-ttu-id="1f938-118">UINT16 Депсораррайсизе</span><span class="sxs-lookup"><span data-stu-id="1f938-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="1f938-119">UINT16 Миплевелс</span><span class="sxs-lookup"><span data-stu-id="1f938-119">UINT16 mipLevels</span></span>

<span data-ttu-id="1f938-120">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="1f938-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="1f938-121">UINT sampleCount</span><span class="sxs-lookup"><span data-stu-id="1f938-121">UINT sampleCount</span></span>

<span data-ttu-id="1f938-122">UINT Самплекуалити</span><span class="sxs-lookup"><span data-stu-id="1f938-122">UINT sampleQuality</span></span>

<span data-ttu-id="1f938-123">[**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)</span><span class="sxs-lookup"><span data-stu-id="1f938-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="1f938-124">[**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)</span><span class="sxs-lookup"><span data-stu-id="1f938-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="1f938-125">**статический встроенный буфер (const D3D12 \_ \_ сведения о выделении ресурсов \_& ресаллоЦинфо, флаги \_ \_ флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="1f938-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-126">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1f938-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1f938-127">[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо</span><span class="sxs-lookup"><span data-stu-id="1f938-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="1f938-128">участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="1f938-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="1f938-129">**статический встроенный буфер (ширина UINT64, флаги \_ \_ флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None, выравнивание UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="1f938-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-130">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1f938-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1f938-131">Ширина UINT64</span><span class="sxs-lookup"><span data-stu-id="1f938-131">UINT64 width</span></span>

<span data-ttu-id="1f938-132">участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="1f938-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="1f938-133">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="1f938-134">**static Inline Tex1D ( \_ Формат формата DXGI, ширина UINT64, UINT16 размера массива = 1, UINT16 миплевелс = 0, флаги \_ \_ флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None, \_ D3D12 \_ Макет макета = D3D12 \_ \_ Макет текстуры \_ Unknown, выравнивание UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="1f938-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-135">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1f938-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1f938-136">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="1f938-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="1f938-137">Ширина UINT64</span><span class="sxs-lookup"><span data-stu-id="1f938-137">UINT64 width</span></span>

<span data-ttu-id="1f938-138">участие UINT16 размера массива = 1</span><span class="sxs-lookup"><span data-stu-id="1f938-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="1f938-139">участие UINT16 Миплевелс = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="1f938-140">участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="1f938-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="1f938-141">участие [**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) — \_ \_ НЕизвестный макет текстуры \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="1f938-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="1f938-142">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="1f938-143">**static Inline Tex2D ( \_ Формат формата DXGI, ширина UINT64, высота uint, UINT16 размера массива = 1, UINT16 миплевелс = 0, uint sampleCount = 1, uint самплекуалити = 0, флаги \_ \_ флагов ресурсов D3D12 = D3D12, \_ \_ флаг \_ , параметр D3D12, макет \_ текстуры \_ = \_ D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f938-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-144">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1f938-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1f938-145">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="1f938-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="1f938-146">Ширина UINT64</span><span class="sxs-lookup"><span data-stu-id="1f938-146">UINT64 width</span></span>

<span data-ttu-id="1f938-147">Высота UINT</span><span class="sxs-lookup"><span data-stu-id="1f938-147">UINT height</span></span>

<span data-ttu-id="1f938-148">участие UINT16 размера массива = 1</span><span class="sxs-lookup"><span data-stu-id="1f938-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="1f938-149">участие UINT16 Миплевелс = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="1f938-150">участие UINT sampleCount = 1</span><span class="sxs-lookup"><span data-stu-id="1f938-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="1f938-151">участие UINT Самплекуалити = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="1f938-152">участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="1f938-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="1f938-153">участие [**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) — \_ \_ НЕизвестный макет текстуры \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="1f938-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="1f938-154">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="1f938-155">**статическое встроенное Tex3D ( \_ Формат формата DXGI, ширина UINT64, высота uint, длина UInt16, UInt16 миплевелс = 0, \_ \_ Флаги флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None, D3D12 макет \_ \_ макета текстуры = D3D12 \_ \_ Макет текстуры \_ Unknown, выравнивание UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="1f938-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-156">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1f938-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1f938-157">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="1f938-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="1f938-158">Ширина UINT64</span><span class="sxs-lookup"><span data-stu-id="1f938-158">UINT64 width</span></span>

<span data-ttu-id="1f938-159">Высота UINT</span><span class="sxs-lookup"><span data-stu-id="1f938-159">UINT height</span></span>

<span data-ttu-id="1f938-160">Глубина UINT16</span><span class="sxs-lookup"><span data-stu-id="1f938-160">UINT16 depth</span></span>

<span data-ttu-id="1f938-161">участие UINT16 Миплевелс = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="1f938-162">участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="1f938-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="1f938-163">участие [**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) — \_ \_ НЕизвестный макет текстуры \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="1f938-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="1f938-164">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="1f938-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="1f938-165">**Константа встроенной глубины ()**</span><span class="sxs-lookup"><span data-stu-id="1f938-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-166">Если Dimension = = [**D3D12 \_ TEXTURE3D \_ измерения**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ , возвращает депсораррайсизе.</span><span class="sxs-lookup"><span data-stu-id="1f938-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="1f938-167">Если Dimension! = D3D12 \_ \_ TEXTURE3D измерения \_ , возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="1f938-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-168">**Inline размера массива () const**</span><span class="sxs-lookup"><span data-stu-id="1f938-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-169">Если Dimension! = D3D12 \_ \_ TEXTURE3D ресурса измерения \_ , возвращает депсораррайсизе.</span><span class="sxs-lookup"><span data-stu-id="1f938-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="1f938-170">Если Dimension = = D3D12 \_ \_ TEXTURE3D измерения \_ , возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="1f938-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="1f938-171">См. раздел [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.</span><span class="sxs-lookup"><span data-stu-id="1f938-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-172">**Inline Планекаунт (ID3D12Device \* пдевице) const**</span><span class="sxs-lookup"><span data-stu-id="1f938-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-173">Возвращает D3D12GetFormatPlaneCount (Пдевице, Format).</span><span class="sxs-lookup"><span data-stu-id="1f938-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="1f938-174">См. раздел [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="1f938-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="1f938-175">**Встроенные подресурсы (ID3D12Device \* пдевице) const**</span><span class="sxs-lookup"><span data-stu-id="1f938-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-176">Возвращает количество подресурсов, вычисленное как Миплевелс \* размера массива () \* Планекаунт (пдевице).</span><span class="sxs-lookup"><span data-stu-id="1f938-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f938-177">**Inline Калксубресаурце (UINT Мипслице, UINT Аррайслице, UINT Планеслице)**</span><span class="sxs-lookup"><span data-stu-id="1f938-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-178">Вычисляет индекс подресурса с помощью [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span><span class="sxs-lookup"><span data-stu-id="1f938-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f938-179">**Оператор const D3D12 \_ ресурса \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="1f938-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-180">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="1f938-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-181">**оператор = = (const D3D12 \_ Resource \_ DESC& l, const D3D12 \_ ресурс \_ DESC& r)**</span><span class="sxs-lookup"><span data-stu-id="1f938-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-182">Возвращает значение true, если все члены каждой структуры идентичны.</span><span class="sxs-lookup"><span data-stu-id="1f938-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-183">**operator! = (const D3D12 \_ ресурс \_ DESC& l, const D3D12 \_ Resource \_ DESC& r)**</span><span class="sxs-lookup"><span data-stu-id="1f938-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="1f938-184">Возвращает значение false, если все члены каждой структуры идентичны.</span><span class="sxs-lookup"><span data-stu-id="1f938-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f938-185">Требования</span><span class="sxs-lookup"><span data-stu-id="1f938-185">Requirements</span></span>



| <span data-ttu-id="1f938-186">Требование</span><span class="sxs-lookup"><span data-stu-id="1f938-186">Requirement</span></span> | <span data-ttu-id="1f938-187">Значение</span><span class="sxs-lookup"><span data-stu-id="1f938-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1f938-188">Header</span><span class="sxs-lookup"><span data-stu-id="1f938-188">Header</span></span><br/> | <dl> <span data-ttu-id="1f938-189"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f938-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f938-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f938-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f938-191">**D3D12 \_ ресурс \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1f938-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="1f938-192">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="1f938-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

