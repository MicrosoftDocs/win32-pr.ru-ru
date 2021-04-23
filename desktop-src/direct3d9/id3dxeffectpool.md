---
description: Приложения используют интерфейс ID3DXEffectPool для задания параметров, которые будут совместно использоваться различными эффектами. См. раздел Совместное использование параметров в клонировании и совместном использовании (Direct3D 9). У этого интерфейса нет методов.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Интерфейс ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424338"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="c3504-105">Интерфейс ID3DXEffectPool</span><span class="sxs-lookup"><span data-stu-id="c3504-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="c3504-106">Приложения используют интерфейс **ID3DXEffectPool** для задания параметров, которые будут совместно использоваться различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="c3504-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="c3504-107">См. раздел Совместное использование параметров в [клонировании и совместном использовании (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="c3504-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="c3504-108">У этого интерфейса нет методов.</span><span class="sxs-lookup"><span data-stu-id="c3504-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="c3504-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="c3504-109">Members</span></span>

<span data-ttu-id="c3504-110">Интерфейс **ID3DXEffectPool** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="c3504-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3504-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3504-111">Remarks</span></span>

<span data-ttu-id="c3504-112">Интерфейс ID3DXEffectPool получается путем вызова [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span><span class="sxs-lookup"><span data-stu-id="c3504-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="c3504-113">Тип LPD3DXEFFECTPOOL определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c3504-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="c3504-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c3504-114">Requirements</span></span>



| <span data-ttu-id="c3504-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c3504-115">Requirement</span></span> | <span data-ttu-id="c3504-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c3504-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3504-117">Header</span><span class="sxs-lookup"><span data-stu-id="c3504-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3504-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3504-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c3504-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3504-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3504-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3504-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c3504-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3504-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3504-122">Интерфейсы эффектов</span><span class="sxs-lookup"><span data-stu-id="c3504-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
