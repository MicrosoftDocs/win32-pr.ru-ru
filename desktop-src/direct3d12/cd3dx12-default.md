---
title: Структура CD3DX12_DEFAULT (D3dx12. h)
description: Передает D3D12 \_ по умолчанию в конструктор для каждой вспомогательной структуры. Эта структура просто используется в качестве механизма установки параметров по умолчанию для других вспомогательных структур.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Структура CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647821"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="812db-105">\_Структура по умолчанию CD3DX12</span><span class="sxs-lookup"><span data-stu-id="812db-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="812db-106">Передает D3D12 \_ по умолчанию в конструктор для каждой вспомогательной структуры.</span><span class="sxs-lookup"><span data-stu-id="812db-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="812db-107">Эта структура просто используется в качестве механизма установки параметров по умолчанию для других вспомогательных структур.</span><span class="sxs-lookup"><span data-stu-id="812db-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="812db-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="812db-108">Remarks</span></span>

<span data-ttu-id="812db-109">Эта структура объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="812db-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="812db-110">Передает D3D12 \_ по умолчанию в конструктор для каждой вспомогательной структуры.</span><span class="sxs-lookup"><span data-stu-id="812db-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="812db-111">Например, следующий конструктор объявлен в d3dx12. h:</span><span class="sxs-lookup"><span data-stu-id="812db-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="812db-112">\_Дескриптор CD3DX12 \_ ЦП \_ (CD3DX12 \_ по умолчанию) {PTR = 0;}</span><span class="sxs-lookup"><span data-stu-id="812db-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="812db-113">Требования</span><span class="sxs-lookup"><span data-stu-id="812db-113">Requirements</span></span>



| <span data-ttu-id="812db-114">Требование</span><span class="sxs-lookup"><span data-stu-id="812db-114">Requirement</span></span> | <span data-ttu-id="812db-115">Значение</span><span class="sxs-lookup"><span data-stu-id="812db-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="812db-116">Header</span><span class="sxs-lookup"><span data-stu-id="812db-116">Header</span></span><br/> | <dl> <span data-ttu-id="812db-117"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="812db-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="812db-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="812db-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="812db-119">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="812db-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





