---
description: Описывает вектор с двумя компонентами, включая перегрузки операторов и приведения типов.
ms.assetid: e61ec1c8-00b5-491f-8fb1-be97218f6c68
title: Структура D3DXVECTOR2 (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: f7f54dc67c038d7c22929b67c59e6b0331a5e545
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714048"
---
# <a name="d3dxvector2-structure-d3dx9mathh"></a><span data-ttu-id="9cc95-103">Структура D3DXVECTOR2 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9cc95-103">D3DXVECTOR2 structure (D3dx9math.h)</span></span>

<span data-ttu-id="9cc95-104">Описывает вектор с двумя компонентами, включая перегрузки операторов и приведения типов.</span><span class="sxs-lookup"><span data-stu-id="9cc95-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cc95-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="9cc95-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9cc95-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9cc95-107">**x**</span><span class="sxs-lookup"><span data-stu-id="9cc95-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="9cc95-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cc95-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9cc95-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="9cc95-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="9cc95-110">**y**</span><span class="sxs-lookup"><span data-stu-id="9cc95-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="9cc95-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cc95-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9cc95-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="9cc95-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cc95-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cc95-113">Remarks</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="9cc95-114">Расширения D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="9cc95-114">D3DXVECTOR2 Extensions</span></span>

<span data-ttu-id="9cc95-115">D3DXVECTOR2 имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="9cc95-115">D3DXVECTOR2 has the following C++ extensions.</span></span>


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

typedef struct D3DXVECTOR2_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR2_16F() {};
    D3DXVECTOR2_16F( CONST FLOAT * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR2_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR2_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y;

} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
        
```



## <a name="requirements"></a><span data-ttu-id="9cc95-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9cc95-116">Requirements</span></span>



| <span data-ttu-id="9cc95-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9cc95-117">Requirement</span></span> | <span data-ttu-id="9cc95-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9cc95-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc95-119">Header</span><span class="sxs-lookup"><span data-stu-id="9cc95-119">Header</span></span><br/> | <dl> <span data-ttu-id="9cc95-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc95-120"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc95-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cc95-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc95-122">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="9cc95-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
