---
title: Структура CD3DX12_BOX (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру бокса D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Структура CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694110"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="b4119-104">\_Структура Box CD3DX12</span><span class="sxs-lookup"><span data-stu-id="b4119-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="b4119-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ бокса D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="b4119-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4119-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4119-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="b4119-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b4119-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4119-108">**\_Поле CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="b4119-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-109">Создает новый, неинициализированный экземпляр \_ поля CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="b4119-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="b4119-110">**явное \_ поле CD3DX12 (const D3D12 \_ Box& o)**</span><span class="sxs-lookup"><span data-stu-id="b4119-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-111">Создает новый экземпляр \_ поля CD3DX12, инициализированного с содержимым другой структуры [**\_ Box D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="b4119-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4119-112">**Explicit CD3DX12 \_ (слева, длинное право)**</span><span class="sxs-lookup"><span data-stu-id="b4119-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-113">Создает новый экземпляр \_ поля CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b4119-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="b4119-114">ДЛИННое левое</span><span class="sxs-lookup"><span data-stu-id="b4119-114">LONG Left</span></span>

<span data-ttu-id="b4119-115">ДЛИННое право</span><span class="sxs-lookup"><span data-stu-id="b4119-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="b4119-116">**Explicit CD3DX12 \_ (длинный левый, длинный верхний, длинный правый, длинный нижний)**</span><span class="sxs-lookup"><span data-stu-id="b4119-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-117">Создает новый экземпляр \_ поля CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b4119-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="b4119-118">ДЛИННое левое</span><span class="sxs-lookup"><span data-stu-id="b4119-118">LONG Left</span></span>

<span data-ttu-id="b4119-119">ДЛИННое сверху</span><span class="sxs-lookup"><span data-stu-id="b4119-119">LONG Top</span></span>

<span data-ttu-id="b4119-120">ДЛИННое право</span><span class="sxs-lookup"><span data-stu-id="b4119-120">LONG Right</span></span>

<span data-ttu-id="b4119-121">ДЛИННое нижнее</span><span class="sxs-lookup"><span data-stu-id="b4119-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="b4119-122">**явный CD3DX12 \_ (длинный левый, длинный верхний, длинный передний, длинный правый, длинный нижний, длинный)**</span><span class="sxs-lookup"><span data-stu-id="b4119-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-123">Создает новый экземпляр \_ поля CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b4119-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="b4119-124">ДЛИННое левое</span><span class="sxs-lookup"><span data-stu-id="b4119-124">LONG Left</span></span>

<span data-ttu-id="b4119-125">ДЛИННое сверху</span><span class="sxs-lookup"><span data-stu-id="b4119-125">LONG Top</span></span>

<span data-ttu-id="b4119-126">ДЛИННая спереди</span><span class="sxs-lookup"><span data-stu-id="b4119-126">LONG Front</span></span>

<span data-ttu-id="b4119-127">ДЛИННое право</span><span class="sxs-lookup"><span data-stu-id="b4119-127">LONG Right</span></span>

<span data-ttu-id="b4119-128">ДЛИННое нижнее</span><span class="sxs-lookup"><span data-stu-id="b4119-128">LONG Bottom</span></span>

<span data-ttu-id="b4119-129">ДЛИННая резервная копия</span><span class="sxs-lookup"><span data-stu-id="b4119-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="b4119-130">**~ CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="b4119-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-131">Уничтожает экземпляр \_ поля CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="b4119-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="b4119-132">**Оператор const D3D12 \_ BOX& () const**</span><span class="sxs-lookup"><span data-stu-id="b4119-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b4119-133">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="b4119-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4119-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b4119-134">Requirements</span></span>



| <span data-ttu-id="b4119-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b4119-135">Requirement</span></span> | <span data-ttu-id="b4119-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b4119-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4119-137">Header</span><span class="sxs-lookup"><span data-stu-id="b4119-137">Header</span></span><br/> | <dl> <span data-ttu-id="b4119-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4119-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4119-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4119-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4119-140">**\_Поле D3D12**</span><span class="sxs-lookup"><span data-stu-id="b4119-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="b4119-141">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="b4119-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





