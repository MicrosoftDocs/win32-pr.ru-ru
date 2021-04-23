---
description: Предоставляет перегрузки операторов и приведения типов для структур D3DXFLOAT16.
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: Расширения D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f97e8917f453e7c2c2db99b8f894d557d7b7909f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081860"
---
# <a name="d3dxfloat16-extensions"></a><span data-ttu-id="30f60-103">Расширения D3DXFLOAT16</span><span class="sxs-lookup"><span data-stu-id="30f60-103">D3DXFLOAT16 Extensions</span></span>

<span data-ttu-id="30f60-104">Предоставляет перегрузки операторов и приведения типов для структур [**D3DXFLOAT16**](d3dxfloat16.md) .</span><span class="sxs-lookup"><span data-stu-id="30f60-104">Supplies operator overloads and type casts for [**D3DXFLOAT16**](d3dxfloat16.md) structures.</span></span>

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

<span data-ttu-id="30f60-105">Производные типы: \* LPD3DXFLOAT16</span><span class="sxs-lookup"><span data-stu-id="30f60-105">Derived types: \*LPD3DXFLOAT16</span></span>

## <a name="members"></a><span data-ttu-id="30f60-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="30f60-106">Members</span></span>

<span data-ttu-id="30f60-107">Дополнительные сведения о членах структуры см. в разделе D3DXFLOAT16.</span><span class="sxs-lookup"><span data-stu-id="30f60-107">For more information about structure members, refer to D3DXFLOAT16.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f60-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30f60-108">Remarks</span></span>

<span data-ttu-id="30f60-109">Перегрузки операторов и приведения типов для этой структуры реализуются в d3dx9math. inl.</span><span class="sxs-lookup"><span data-stu-id="30f60-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f60-110">Требования</span><span class="sxs-lookup"><span data-stu-id="30f60-110">Requirements</span></span>



| <span data-ttu-id="30f60-111">Требование</span><span class="sxs-lookup"><span data-stu-id="30f60-111">Requirement</span></span> | <span data-ttu-id="30f60-112">Значение</span><span class="sxs-lookup"><span data-stu-id="30f60-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30f60-113">Header</span><span class="sxs-lookup"><span data-stu-id="30f60-113">Header</span></span><br/> | <dl> <span data-ttu-id="30f60-114"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f60-114"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f60-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30f60-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f60-116">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="30f60-116">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




