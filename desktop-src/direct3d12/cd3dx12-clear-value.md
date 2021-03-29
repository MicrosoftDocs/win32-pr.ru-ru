---
title: Структура CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12ного \_ \_ значения.
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Структура CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647823"
---
# <a name="cd3dx12_clear_value-structure"></a><span data-ttu-id="e86e8-104">\_Структура открытого \_ значения CD3DX12</span><span class="sxs-lookup"><span data-stu-id="e86e8-104">CD3DX12\_CLEAR\_VALUE structure</span></span>

<span data-ttu-id="e86e8-105">Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12ного \_ \_ значения**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="e86e8-105">A helper structure to enable easy initialization of a [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86e8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e86e8-106">Syntax</span></span>


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a><span data-ttu-id="e86e8-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e86e8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e86e8-108">**CD3DX12ое \_ \_ значение Clear ()**</span><span class="sxs-lookup"><span data-stu-id="e86e8-108">**CD3DX12\_CLEAR\_VALUE()**</span></span>
</dt> <dd>

<span data-ttu-id="e86e8-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ значения Clear.</span><span class="sxs-lookup"><span data-stu-id="e86e8-109">Creates a new, uninitialized, instance of a CD3DX12\_CLEAR\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="e86e8-110">**явное \_ CD3DX12 \_ значение Clear (const D3D12 \_ очистить \_ значение &o)**</span><span class="sxs-lookup"><span data-stu-id="e86e8-110">**explicit CD3DX12\_CLEAR\_VALUE(const D3D12\_CLEAR\_VALUE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e86e8-111">Создает новый экземпляр \_ значения CD3DX12 Clear \_ , инициализированного с содержимым другой структуры [**D3D12 \_ clear \_ value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="e86e8-111">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initialized with the contents of another [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e86e8-112">**CD3DX12 \_ \_ значение Clear ( \_ Формат формата DXGI, КОНСТАНТа с плавающей запятой, цвет \[ 4 \] )**</span><span class="sxs-lookup"><span data-stu-id="e86e8-112">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, const FLOAT color\[ 4 \])**</span></span>
</dt> <dd>

<span data-ttu-id="e86e8-113">Создает новый экземпляр \_ значения CD3DX12 Clear \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e86e8-113">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="e86e8-114">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="e86e8-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="e86e8-115">Цвет 4 с плавающей запятой \[\]</span><span class="sxs-lookup"><span data-stu-id="e86e8-115">FLOAT color\[ 4 \]</span></span>

</dd> <dt>

<span data-ttu-id="e86e8-116">**CD3DX12 \_ \_ значение Clear ( \_ Формат формата DXGI, глубина float, набор элементов UINT8)**</span><span class="sxs-lookup"><span data-stu-id="e86e8-116">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, FLOAT depth, UINT8 stencil)**</span></span>
</dt> <dd>

<span data-ttu-id="e86e8-117">Создает новый экземпляр \_ значения CD3DX12 Clear \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e86e8-117">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="e86e8-118">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="e86e8-118">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="e86e8-119">Глубина плавающего числа</span><span class="sxs-lookup"><span data-stu-id="e86e8-119">FLOAT depth</span></span>

<span data-ttu-id="e86e8-120">Набор элементов UINT8</span><span class="sxs-lookup"><span data-stu-id="e86e8-120">UINT8 stencil</span></span>

</dd> <dt>

<span data-ttu-id="e86e8-121">**Оператор const D3D12 \_ clear \_ значение& () const**</span><span class="sxs-lookup"><span data-stu-id="e86e8-121">**operator const D3D12\_CLEAR\_VALUE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e86e8-122">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="e86e8-122">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e86e8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e86e8-123">Requirements</span></span>



| <span data-ttu-id="e86e8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e86e8-124">Requirement</span></span> | <span data-ttu-id="e86e8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e86e8-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e86e8-126">Header</span><span class="sxs-lookup"><span data-stu-id="e86e8-126">Header</span></span><br/> | <dl> <span data-ttu-id="e86e8-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e86e8-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86e8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e86e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86e8-129">**D3D12ое \_ \_ значение**</span><span class="sxs-lookup"><span data-stu-id="e86e8-129">**D3D12\_CLEAR\_VALUE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[<span data-ttu-id="e86e8-130">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="e86e8-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

