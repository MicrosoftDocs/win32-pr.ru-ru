---
description: Этот макрос создает значение, используемое вопросом для начала выполнения запроса.
ms.assetid: 21b8a2b0-d18f-4412-b655-3a913b7312ee
title: D3DISSUE_BEGIN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_BEGIN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 90d932176a70159d31a239a9a37422b474acb485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355080"
---
# <a name="d3dissue_begin"></a><span data-ttu-id="d5742-103">\_Начало D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="d5742-103">D3DISSUE\_BEGIN</span></span>

<span data-ttu-id="d5742-104">Этот макрос создает значение, используемое [**вопросом**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) для начала выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="d5742-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query begin.</span></span>

``` syntax
#define D3DISSUE_BEGIN (1 << 1)
```

## <a name="remarks"></a><span data-ttu-id="d5742-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5742-105">Remarks</span></span>

<span data-ttu-id="d5742-106">D3DISSUE \_ Begin является допустимым для следующего типа запроса.</span><span class="sxs-lookup"><span data-stu-id="d5742-106">D3DISSUE\_BEGIN is valid for the following query type.</span></span>

-   <span data-ttu-id="d5742-107">D3DQUERYTYPE \_ перекрытия</span><span class="sxs-lookup"><span data-stu-id="d5742-107">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="d5742-108">Требования</span><span class="sxs-lookup"><span data-stu-id="d5742-108">Requirements</span></span>



| <span data-ttu-id="d5742-109">Требование</span><span class="sxs-lookup"><span data-stu-id="d5742-109">Requirement</span></span> | <span data-ttu-id="d5742-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d5742-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5742-111">Header</span><span class="sxs-lookup"><span data-stu-id="d5742-111">Header</span></span><br/> | <dl> <span data-ttu-id="d5742-112"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5742-112"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5742-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5742-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5742-114">Макросы</span><span class="sxs-lookup"><span data-stu-id="d5742-114">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="d5742-115">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="d5742-115">**D3DISSUE\_END**</span></span>](d3dissue-end.md)
</dt> <dt>

[<span data-ttu-id="d5742-116">**D3DGETDATA \_ запись на диск**</span><span class="sxs-lookup"><span data-stu-id="d5742-116">**D3DGETDATA\_FLUSH**</span></span>](d3dgetdata-flush.md)
</dt> <dt>

[<span data-ttu-id="d5742-117">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="d5742-117">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
