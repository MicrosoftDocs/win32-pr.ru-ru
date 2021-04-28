---
description: D3DXMATRIXA16 Structure (D3dx9math. h) — матрица 4x4, 16-байтовое с согласованием, которая содержит методы и перегрузки операторов.
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Структура D3DXMATRIXA16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094212"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="cb3c3-103">Структура D3DXMATRIXA16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cb3c3-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="cb3c3-104">Матрица 4x4, 16-байтовое с согласованием, которая содержит методы и перегрузки операторов.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb3c3-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="cb3c3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="cb3c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb3c3-107">**\_иж**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="cb3c3-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cb3c3-109">Компонент (i, j) матрицы, где i — это номер строки, а j — номер столбца.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="cb3c3-110">Например, \_ 34 означает то же, что и \[ ₃ ₄ \] , компонент в третьей строке и четвертом столбце.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb3c3-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb3c3-111">Remarks</span></span>

<span data-ttu-id="cb3c3-112">При использовании математических функций D3DX для повышения производительности процессоров Intel Pentium 4 оптимизирована сопоставленная 16-байтная матрица.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="cb3c3-113">Матрицы согласовываются независимо от места их создания: в стеке программы, в куче или в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="cb3c3-114">Выравнивание выполняется с помощью \_ \_ declspec (выравнивание (16)), которое работает с Visual C++ .net и Visual C++ 6,0 только при установке пакета процессора.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="cb3c3-115">К сожалению, нет способа обнаружить пакет процессора, поэтому выравнивание байтов по умолчанию включено только с Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="cb3c3-116">Векторы и кватернион не имеют согласованного байта в D3DX.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="cb3c3-117">При использовании векторов и кватернионов с математическими функциями D3DX используйте \_ declspec (выровняйте (16)) для создания векторов с согласованием байтов и кватернионов, так как они будут выполняться значительно лучше.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="cb3c3-118">Определение \_ declspec показано здесь.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="cb3c3-119">Другие компиляторы преобразуют D3DXMATRIXA16 как D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="cb3c3-120">Использование этой структуры на компиляторе, который фактически не выравнивает матрицу, может быть проблематичным, так как не будет предоставлять ошибки, не пропускаемые выравниванием.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="cb3c3-121">Например, если объект D3DXMATRIXA16 находится внутри структуры или класса, [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) может выполняться с плотной упаковкой (игнорируя 16-байтные границы).</span><span class="sxs-lookup"><span data-stu-id="cb3c3-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="cb3c3-122">Это приведет к прерыванию сборки, если бы компилятору пришлось добавлять к нему выровняйте матрицу.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="cb3c3-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="cb3c3-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="cb3c3-124">**D3DXMATRIXA16** имеет следующие расширения C++.</span><span class="sxs-lookup"><span data-stu-id="cb3c3-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a><span data-ttu-id="cb3c3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cb3c3-125">Requirements</span></span>



| <span data-ttu-id="cb3c3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cb3c3-126">Requirement</span></span> | <span data-ttu-id="cb3c3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cb3c3-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3c3-128">Header</span><span class="sxs-lookup"><span data-stu-id="cb3c3-128">Header</span></span><br/> | <dl> <span data-ttu-id="cb3c3-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3c3-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb3c3-130">См. также</span><span class="sxs-lookup"><span data-stu-id="cb3c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3c3-131">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="cb3c3-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="cb3c3-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="cb3c3-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
