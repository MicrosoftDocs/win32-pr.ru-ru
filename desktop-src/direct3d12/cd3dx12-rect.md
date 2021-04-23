---
title: Структура CD3DX12_RECT (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру Rect D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Структура CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713515"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="5da2b-104">\_Структура Rect CD3DX12</span><span class="sxs-lookup"><span data-stu-id="5da2b-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="5da2b-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ Rect D3D12**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="5da2b-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da2b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5da2b-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="5da2b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5da2b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5da2b-108">**CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="5da2b-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="5da2b-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="5da2b-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="5da2b-110">**явный CD3DX12 \_ Rect (const D3D12 \_ Rect& o)**</span><span class="sxs-lookup"><span data-stu-id="5da2b-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="5da2b-111">Создает новый экземпляр CD3DX12 \_ Rect, инициализируемый с помощью содержимого другой структуры [**D3D12 \_ Rect**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="5da2b-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5da2b-112">**явный \_ прямоугольник CD3DX12 (длинный левый, длинный верхний, длинный правый, длинный нижний)**</span><span class="sxs-lookup"><span data-stu-id="5da2b-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="5da2b-113">Создает новый экземпляр CD3DX12 \_ Rect, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5da2b-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="5da2b-114">ДЛИННое левое</span><span class="sxs-lookup"><span data-stu-id="5da2b-114">LONG Left</span></span>

<span data-ttu-id="5da2b-115">ДЛИННое сверху</span><span class="sxs-lookup"><span data-stu-id="5da2b-115">LONG Top</span></span>

<span data-ttu-id="5da2b-116">ДЛИННое право</span><span class="sxs-lookup"><span data-stu-id="5da2b-116">LONG Right</span></span>

<span data-ttu-id="5da2b-117">ДЛИННое нижнее</span><span class="sxs-lookup"><span data-stu-id="5da2b-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="5da2b-118">**~ CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="5da2b-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="5da2b-119">Уничтожает экземпляр \_ Rect CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="5da2b-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="5da2b-120">**Константа operator const D3D12 \_ RECT& () const**</span><span class="sxs-lookup"><span data-stu-id="5da2b-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5da2b-121">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="5da2b-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5da2b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5da2b-122">Requirements</span></span>



| <span data-ttu-id="5da2b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5da2b-123">Requirement</span></span> | <span data-ttu-id="5da2b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5da2b-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5da2b-125">Header</span><span class="sxs-lookup"><span data-stu-id="5da2b-125">Header</span></span><br/> | <dl> <span data-ttu-id="5da2b-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5da2b-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da2b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5da2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da2b-128">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="5da2b-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="5da2b-129">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="5da2b-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





