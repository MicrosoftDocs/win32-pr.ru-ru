---
description: Описывает вектор с четырьмя компонентами, включая перегрузки операторов и приведения типов.
ms.assetid: c6348346-f317-48ed-a369-e39fdb4dc1d6
title: Структура D3DXVECTOR4 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ce65fe5cc6de9d842fb7c93b1089e53b9b27920c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424498"
---
# <a name="d3dxvector4-structure-d3dx10mathh"></a><span data-ttu-id="6c76a-103">Структура D3DXVECTOR4 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6c76a-103">D3DXVECTOR4 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="6c76a-104">Описывает вектор с четырьмя компонентами, включая перегрузки операторов и приведения типов.</span><span class="sxs-lookup"><span data-stu-id="6c76a-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c76a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c76a-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="6c76a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6c76a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c76a-107">**x**</span><span class="sxs-lookup"><span data-stu-id="6c76a-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="6c76a-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c76a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c76a-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="6c76a-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="6c76a-110">**y**</span><span class="sxs-lookup"><span data-stu-id="6c76a-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="6c76a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c76a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c76a-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="6c76a-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="6c76a-113">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="6c76a-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="6c76a-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c76a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c76a-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="6c76a-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="6c76a-116">**w**</span><span class="sxs-lookup"><span data-stu-id="6c76a-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="6c76a-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c76a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c76a-118">Компонент w-Component.</span><span class="sxs-lookup"><span data-stu-id="6c76a-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c76a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c76a-119">Remarks</span></span>

<span data-ttu-id="6c76a-120">**D3DXVECTOR4** имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="6c76a-120">**D3DXVECTOR4** has the following C++ extensions.</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="6c76a-121">Расширения D3DXVECTOR4</span><span class="sxs-lookup"><span data-stu-id="6c76a-121">D3DXVECTOR4 Extensions</span></span>


```
typedef struct D3DXVECTOR4
{
#ifdef __cplusplus
public:
    D3DXVECTOR4() {};
    D3DXVECTOR4( CONST FLOAT* );
    D3DXVECTOR4( CONST D3DXFLOAT16 * );
    D3DXVECTOR4( CONST D3DVECTOR& xyz, FLOAT w );
    D3DXVECTOR4( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR4& operator += ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator -= ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator *= ( FLOAT );
    D3DXVECTOR4& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR4 operator + () const;
    D3DXVECTOR4 operator - () const;

    // binary operators
    D3DXVECTOR4 operator + ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator - ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator * ( FLOAT ) const;
    D3DXVECTOR4 operator / ( FLOAT ) const;

    friend D3DXVECTOR4 operator * ( FLOAT, CONST D3DXVECTOR4& );

    BOOL operator == ( CONST D3DXVECTOR4& ) const;
    BOOL operator != ( CONST D3DXVECTOR4& ) const;

public:
#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
        
```



## <a name="requirements"></a><span data-ttu-id="6c76a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6c76a-122">Requirements</span></span>



| <span data-ttu-id="6c76a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6c76a-123">Requirement</span></span> | <span data-ttu-id="6c76a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6c76a-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c76a-125">Header</span><span class="sxs-lookup"><span data-stu-id="6c76a-125">Header</span></span><br/> | <dl> <span data-ttu-id="6c76a-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c76a-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c76a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c76a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c76a-128">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="6c76a-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
