---
description: Предоставляет следующие перегрузки операторов и приведения типов для структур D3DXPLANE.
ms.assetid: 05f80b68-fb2b-4fd7-94e9-e5b40968c4aa
title: Расширения D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3ff8f68283cd81e6647fcdea480ac19b48547cab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713465"
---
# <a name="d3dxplane-extensions"></a><span data-ttu-id="19596-103">Расширения D3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="19596-103">D3DXPLANE Extensions</span></span>

<span data-ttu-id="19596-104">Предоставляет следующие перегрузки операторов и приведения типов для структур [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="19596-104">Supplies the following operator overloads and type casts for [**D3DXPLANE**](d3dxplane.md) structures.</span></span>

``` syntax
typedef struct D3DXPLANE
{
#ifdef __cplusplus
public:
    D3DXPLANE() {}
    D3DXPLANE( CONST FLOAT* );
    D3DXPLANE( CONST D3DXFLOAT16* );
    D3DXPLANE( FLOAT a, FLOAT b, FLOAT c, FLOAT d );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXPLANE& operator *= ( FLOAT );
    D3DXPLANE& operator /= ( FLOAT );

    // unary operators
    D3DXPLANE operator + () const;
    D3DXPLANE operator - () const;

    // binary operators
    D3DXPLANE operator * ( FLOAT ) const;
    D3DXPLANE operator / ( FLOAT ) const;

    friend D3DXPLANE operator * ( FLOAT, CONST D3DXPLANE& );

    BOOL operator == ( CONST D3DXPLANE& ) const;
    BOOL operator != ( CONST D3DXPLANE& ) const;

#endif //__cplusplus
    FLOAT a, b, c, d;
} D3DXPLANE, *LPD3DXPLANE;
```

<span data-ttu-id="19596-105">Производные типы: \* LPD3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="19596-105">Derived types: \*LPD3DXPLANE</span></span>

## <a name="remarks"></a><span data-ttu-id="19596-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19596-106">Remarks</span></span>

<span data-ttu-id="19596-107">Дополнительные сведения о членах структуры см. в разделе [**D3DXPLANE**](d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="19596-107">For more information about structure members, refer to [**D3DXPLANE**](d3dxplane.md).</span></span>

<span data-ttu-id="19596-108">Перегрузки операторов и приведения типов для этой структуры реализуются в d3dx9math. inl.</span><span class="sxs-lookup"><span data-stu-id="19596-108">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="19596-109">Требования</span><span class="sxs-lookup"><span data-stu-id="19596-109">Requirements</span></span>



| <span data-ttu-id="19596-110">Требование</span><span class="sxs-lookup"><span data-stu-id="19596-110">Requirement</span></span> | <span data-ttu-id="19596-111">Значение</span><span class="sxs-lookup"><span data-stu-id="19596-111">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19596-112">Header</span><span class="sxs-lookup"><span data-stu-id="19596-112">Header</span></span><br/> | <dl> <span data-ttu-id="19596-113"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19596-113"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19596-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19596-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19596-115">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="19596-115">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




