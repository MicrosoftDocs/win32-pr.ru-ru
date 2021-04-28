---
description: Структура D3DXVECTOR3 (D3DX10Math. h) — описывает вектор с тремя компонентами, включая перегрузки операторов и приведения типов.
ms.assetid: d170cd26-d705-4a31-82b3-f9ea070b6ca4
title: Структура D3DXVECTOR3 (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: 7b43348b6b5683e9fe75c5340fd0c2cab5efe719
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102856"
---
# <a name="d3dxvector3-structure-d3dx10mathh"></a><span data-ttu-id="200b2-103">Структура D3DXVECTOR3 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="200b2-103">D3DXVECTOR3 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="200b2-104">Описывает вектор с тремя компонентами, включая перегрузки операторов и приведения типов.</span><span class="sxs-lookup"><span data-stu-id="200b2-104">Describes a three-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="200b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="200b2-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
```



## <a name="members"></a><span data-ttu-id="200b2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="200b2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="200b2-107">**x**</span><span class="sxs-lookup"><span data-stu-id="200b2-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="200b2-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="200b2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="200b2-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="200b2-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="200b2-110">**y**</span><span class="sxs-lookup"><span data-stu-id="200b2-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="200b2-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="200b2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="200b2-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="200b2-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="200b2-113">**z**</span><span class="sxs-lookup"><span data-stu-id="200b2-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="200b2-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="200b2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="200b2-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="200b2-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="200b2-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="200b2-116">Remarks</span></span>

<span data-ttu-id="200b2-117">**D3DXVECTOR3** имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="200b2-117">**D3DXVECTOR3** has the following C++ extensions.</span></span>

### <a name="d3dxvector3-extensions"></a><span data-ttu-id="200b2-118">Расширения D3DXVECTOR3</span><span class="sxs-lookup"><span data-stu-id="200b2-118">D3DXVECTOR3 Extensions</span></span>


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
        
```



## <a name="requirements"></a><span data-ttu-id="200b2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="200b2-119">Requirements</span></span>



| <span data-ttu-id="200b2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="200b2-120">Requirement</span></span> | <span data-ttu-id="200b2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="200b2-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="200b2-122">Header</span><span class="sxs-lookup"><span data-stu-id="200b2-122">Header</span></span><br/> | <dl> <span data-ttu-id="200b2-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="200b2-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200b2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="200b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200b2-125">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="200b2-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
