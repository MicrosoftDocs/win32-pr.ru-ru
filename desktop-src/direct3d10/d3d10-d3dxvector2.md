---
description: Структура D3DXVECTOR2 (D3DX10Math. h) — описывает вектор с двумя компонентами, включая перегрузки операторов и приведения типов.
ms.assetid: 5b7b4847-b994-48c6-ae3c-e48ee1716ddd
title: Структура D3DXVECTOR2 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 972238650fa23e8b7aa435cd91b36f2caf8a4d9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102861"
---
# <a name="d3dxvector2-structure-d3dx10mathh"></a><span data-ttu-id="8c444-103">Структура D3DXVECTOR2 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8c444-103">D3DXVECTOR2 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="8c444-104">Описывает вектор с двумя компонентами, включая перегрузки операторов и приведения типов.</span><span class="sxs-lookup"><span data-stu-id="8c444-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c444-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c444-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="8c444-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8c444-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c444-107">**x**</span><span class="sxs-lookup"><span data-stu-id="8c444-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="8c444-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c444-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c444-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="8c444-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="8c444-110">**y**</span><span class="sxs-lookup"><span data-stu-id="8c444-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="8c444-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c444-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c444-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="8c444-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c444-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="8c444-113">Remarks</span></span>

<span data-ttu-id="8c444-114">**D3DXVECTOR2** имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="8c444-114">**D3DXVECTOR2** has the following C++ extensions.</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="8c444-115">Расширения D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="8c444-115">D3DXVECTOR2 Extensions</span></span>


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
        
```



## <a name="requirements"></a><span data-ttu-id="8c444-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8c444-116">Requirements</span></span>



| <span data-ttu-id="8c444-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8c444-117">Requirement</span></span> | <span data-ttu-id="8c444-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8c444-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c444-119">Header</span><span class="sxs-lookup"><span data-stu-id="8c444-119">Header</span></span><br/> | <dl> <span data-ttu-id="8c444-120"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c444-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c444-121">См. также</span><span class="sxs-lookup"><span data-stu-id="8c444-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c444-122">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="8c444-122">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
