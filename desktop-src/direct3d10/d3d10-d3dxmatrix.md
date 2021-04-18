---
description: Матрица 4x4, содержащая методы и перегрузки операторов.
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: Структура D3DXMATRIX (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: cae887e2e9a8782cdc7ba159db203c929006c58a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694278"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a><span data-ttu-id="b4374-103">Структура D3DXMATRIX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b4374-103">D3DXMATRIX structure (D3DX10Math.h)</span></span>

<span data-ttu-id="b4374-104">Матрица 4x4, содержащая методы и перегрузки операторов.</span><span class="sxs-lookup"><span data-stu-id="b4374-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4374-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4374-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="b4374-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b4374-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4374-107">**\_иж**</span><span class="sxs-lookup"><span data-stu-id="b4374-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="b4374-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4374-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4374-109">Компонент (i, j) матрицы, где i — это номер строки, а j — номер столбца.</span><span class="sxs-lookup"><span data-stu-id="b4374-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="b4374-110">Например, \_ 34 означает то же, что и \[ ₃ ₄ \] , компонент в третьей строке и четвертом столбце.</span><span class="sxs-lookup"><span data-stu-id="b4374-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4374-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4374-111">Remarks</span></span>

<span data-ttu-id="b4374-112">Программисты C не могут использовать структуру D3DXMATRIX, они должны использовать структуру D3DMATRIX.</span><span class="sxs-lookup"><span data-stu-id="b4374-112">C programmers cannot use the D3DXMATRIX structure, they must use the D3DMATRIX structure.</span></span> <span data-ttu-id="b4374-113">Программисты C++ могут воспользоваться преимуществами перегруженных конструкторов и операторов присваивания, унарных и бинарных (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="b4374-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="b4374-114">В D3DX \_ элемент 34 матрицы проекции не может быть отрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="b4374-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="b4374-115">Если приложению нужно использовать отрицательное значение в этом расположении, необходимо масштабировать всю матрицу проекции на-1.</span><span class="sxs-lookup"><span data-stu-id="b4374-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="b4374-116">Расширения D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="b4374-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="b4374-117">**D3DXMATRIX** имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="b4374-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b4374-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b4374-118">Requirements</span></span>



| <span data-ttu-id="b4374-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b4374-119">Requirement</span></span> | <span data-ttu-id="b4374-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b4374-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4374-121">Header</span><span class="sxs-lookup"><span data-stu-id="b4374-121">Header</span></span><br/> | <dl> <span data-ttu-id="b4374-122"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4374-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4374-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4374-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4374-124">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="b4374-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
