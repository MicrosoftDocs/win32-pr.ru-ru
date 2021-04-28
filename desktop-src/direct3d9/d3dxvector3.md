---
description: Структура D3DXVECTOR3 (D3dx9math. h) — описывает вектор с тремя компонентами, включая перегрузки операторов и приведения типов.
ms.assetid: 4d73de4b-82fe-452a-8a1e-17208f172a03
title: Структура D3DXVECTOR3 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 29d6743f0c0c365911ebbbba66cb4d44f10792e7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097582"
---
# <a name="d3dxvector3-structure-d3dx9mathh"></a><span data-ttu-id="f3e18-103">Структура D3DXVECTOR3 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f3e18-103">D3DXVECTOR3 structure (D3dx9math.h)</span></span>

<span data-ttu-id="f3e18-104">Описывает вектор с тремя компонентами, включая перегрузки операторов и приведения типов.</span><span class="sxs-lookup"><span data-stu-id="f3e18-104">Describes a three-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e18-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3e18-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
```



## <a name="members"></a><span data-ttu-id="f3e18-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f3e18-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3e18-107">**x**</span><span class="sxs-lookup"><span data-stu-id="f3e18-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="f3e18-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3e18-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f3e18-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="f3e18-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="f3e18-110">**y**</span><span class="sxs-lookup"><span data-stu-id="f3e18-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="f3e18-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3e18-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f3e18-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="f3e18-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="f3e18-113">**z**</span><span class="sxs-lookup"><span data-stu-id="f3e18-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="f3e18-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3e18-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f3e18-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="f3e18-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3e18-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="f3e18-116">Remarks</span></span>

### <a name="d3dxvector3-extensions"></a><span data-ttu-id="f3e18-117">Расширения D3DXVECTOR3</span><span class="sxs-lookup"><span data-stu-id="f3e18-117">D3DXVECTOR3 Extensions</span></span>

<span data-ttu-id="f3e18-118">D3DXVECTOR3 имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="f3e18-118">D3DXVECTOR3 has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXVECTOR3 : public D3DVECTOR
{
public:
    D3DXVECTOR3() {};
    D3DXVECTOR3( CONST FLOAT * );
    D3DXVECTOR3( CONST D3DVECTOR& );
    D3DXVECTOR3( CONST D3DXFLOAT16 * );
    D3DXVECTOR3( FLOAT x, FLOAT y, FLOAT z );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR3& operator += ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator -= ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator *= ( FLOAT );
    D3DXVECTOR3& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR3 operator + () const;
    D3DXVECTOR3 operator - () const;

    // binary operators
    D3DXVECTOR3 operator + ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator - ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator * ( FLOAT ) const;
    D3DXVECTOR3 operator / ( FLOAT ) const;

    friend D3DXVECTOR3 operator * ( FLOAT, CONST struct D3DXVECTOR3& );

    BOOL operator == ( CONST D3DXVECTOR3& ) const;
    BOOL operator != ( CONST D3DXVECTOR3& ) const;

} D3DXVECTOR3, *LPD3DXVECTOR3;

#else //!__cplusplus
typedef struct _D3DVECTOR D3DXVECTOR3, *LPD3DXVECTOR3;
#endif //!__cplusplus

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
        
```



## <a name="requirements"></a><span data-ttu-id="f3e18-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f3e18-119">Requirements</span></span>



| <span data-ttu-id="f3e18-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f3e18-120">Requirement</span></span> | <span data-ttu-id="f3e18-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f3e18-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e18-122">Header</span><span class="sxs-lookup"><span data-stu-id="f3e18-122">Header</span></span><br/> | <dl> <span data-ttu-id="f3e18-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e18-123"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e18-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f3e18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e18-125">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="f3e18-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
