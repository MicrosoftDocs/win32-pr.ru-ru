---
description: Этот макрос создает значение, используемое при выдаче запроса.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355083"
---
# <a name="d3dissue_end"></a><span data-ttu-id="5e1a5-103">D3DISSUE \_ конец</span><span class="sxs-lookup"><span data-stu-id="5e1a5-103">D3DISSUE\_END</span></span>

<span data-ttu-id="5e1a5-104">Этот макрос создает значение, используемое [**при выдаче запроса**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) .</span><span class="sxs-lookup"><span data-stu-id="5e1a5-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="5e1a5-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e1a5-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="5e1a5-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e1a5-106">Remarks</span></span>

<span data-ttu-id="5e1a5-107">Этот макрос изменяет состояние запроса на несигнальное.</span><span class="sxs-lookup"><span data-stu-id="5e1a5-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="5e1a5-108">D3DISSUE \_ End допустимо для следующих типов запросов.</span><span class="sxs-lookup"><span data-stu-id="5e1a5-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="5e1a5-109">D3DQUERYTYPE \_ вкаче</span><span class="sxs-lookup"><span data-stu-id="5e1a5-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="5e1a5-110">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="5e1a5-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="5e1a5-111">D3DQUERYTYPE \_ вертексстатс</span><span class="sxs-lookup"><span data-stu-id="5e1a5-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="5e1a5-112">\_Событие D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="5e1a5-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="5e1a5-113">D3DQUERYTYPE \_ перекрытия</span><span class="sxs-lookup"><span data-stu-id="5e1a5-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1a5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5e1a5-114">Requirements</span></span>



| <span data-ttu-id="5e1a5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5e1a5-115">Requirement</span></span> | <span data-ttu-id="5e1a5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5e1a5-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e1a5-117">Header</span><span class="sxs-lookup"><span data-stu-id="5e1a5-117">Header</span></span><br/> | <dl> <span data-ttu-id="5e1a5-118"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e1a5-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e1a5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e1a5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e1a5-120">Макросы</span><span class="sxs-lookup"><span data-stu-id="5e1a5-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5e1a5-121">**\_Начало D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="5e1a5-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="5e1a5-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="5e1a5-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
