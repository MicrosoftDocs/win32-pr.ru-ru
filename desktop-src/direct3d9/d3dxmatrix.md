---
description: Матрица 4x4, содержащая методы и перегрузки операторов.
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: Структура D3DXMATRIX (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 2b09691ff27307e041a79b57e9d32c7e74e5eef1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703744"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a><span data-ttu-id="28d9b-103">Структура D3DXMATRIX (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="28d9b-103">D3DXMATRIX structure (D3dx9math.h)</span></span>

<span data-ttu-id="28d9b-104">Матрица 4x4, содержащая методы и перегрузки операторов.</span><span class="sxs-lookup"><span data-stu-id="28d9b-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d9b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28d9b-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="28d9b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="28d9b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28d9b-107">**\_иж**</span><span class="sxs-lookup"><span data-stu-id="28d9b-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="28d9b-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28d9b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28d9b-109">Компонент (i, j) матрицы, где i — это номер строки, а j — номер столбца.</span><span class="sxs-lookup"><span data-stu-id="28d9b-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="28d9b-110">Например, \_ 34 означает то же, что и \[ ₃ ₄ \] , компонент в третьей строке и четвертом столбце.</span><span class="sxs-lookup"><span data-stu-id="28d9b-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28d9b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28d9b-111">Remarks</span></span>

<span data-ttu-id="28d9b-112">Программисты C не могут использовать структуру D3DXMATRIX, они должны использовать структуру [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="28d9b-112">C programmers cannot use the D3DXMATRIX structure, they must use the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="28d9b-113">Программисты C++ могут воспользоваться преимуществами перегруженных конструкторов и операторов присваивания, унарных и бинарных (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="28d9b-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="28d9b-114">В D3DX \_ элемент 34 матрицы проекции не может быть отрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="28d9b-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="28d9b-115">Если приложению нужно использовать отрицательное значение в этом расположении, необходимо масштабировать всю матрицу проекции на-1.</span><span class="sxs-lookup"><span data-stu-id="28d9b-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="28d9b-116">Расширения D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="28d9b-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="28d9b-117">**D3DXMATRIX** имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="28d9b-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
```



## <a name="requirements"></a><span data-ttu-id="28d9b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="28d9b-118">Requirements</span></span>



| <span data-ttu-id="28d9b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="28d9b-119">Requirement</span></span> | <span data-ttu-id="28d9b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="28d9b-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28d9b-121">Header</span><span class="sxs-lookup"><span data-stu-id="28d9b-121">Header</span></span><br/> | <dl> <span data-ttu-id="28d9b-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d9b-122"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d9b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28d9b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d9b-124">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="28d9b-124">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="28d9b-125">**D3DMATRIX**</span><span class="sxs-lookup"><span data-stu-id="28d9b-125">**D3DMATRIX**</span></span>](d3dmatrix.md)
</dt> </dl>

 

 
