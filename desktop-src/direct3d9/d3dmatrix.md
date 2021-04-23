---
description: Описывает матрицу.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713756"
---
# <a name="d3dmatrix"></a><span data-ttu-id="4f06c-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="4f06c-103">D3DMATRIX</span></span>

<span data-ttu-id="4f06c-104">Описывает матрицу.</span><span class="sxs-lookup"><span data-stu-id="4f06c-104">Describes a matrix.</span></span>

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

<span data-ttu-id="4f06c-105">Производные типы: \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="4f06c-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="4f06c-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="4f06c-106">Members</span></span>



| <span data-ttu-id="4f06c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="4f06c-107">Item</span></span>                                                        | <span data-ttu-id="4f06c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4f06c-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f06c-109"><span id="_ij"></span><span id="_IJ"></span>\_иж</span><span class="sxs-lookup"><span data-stu-id="4f06c-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="4f06c-110">Массив float, который представляет матрицу 4x4, где i — это номер строки, а j — номер столбца.</span><span class="sxs-lookup"><span data-stu-id="4f06c-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="4f06c-111">Например, \_ 34 означает то же, что и \[ ₃ ₄ \] , компонент в третьей строке и четвертом столбце.</span><span class="sxs-lookup"><span data-stu-id="4f06c-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f06c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f06c-112">Remarks</span></span>

<span data-ttu-id="4f06c-113">В Direct3D \_ элемент 34 матрицы проекции не может быть отрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="4f06c-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="4f06c-114">Если приложению нужно использовать отрицательное значение в этом расположении, необходимо масштабировать всю матрицу проекции на-1.</span><span class="sxs-lookup"><span data-stu-id="4f06c-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f06c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4f06c-115">Requirements</span></span>



| <span data-ttu-id="4f06c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4f06c-116">Requirement</span></span> | <span data-ttu-id="4f06c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4f06c-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f06c-118">Header</span><span class="sxs-lookup"><span data-stu-id="4f06c-118">Header</span></span><br/> | <dl> <span data-ttu-id="4f06c-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f06c-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f06c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f06c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f06c-121">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="4f06c-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="4f06c-122">**Преобразование**</span><span class="sxs-lookup"><span data-stu-id="4f06c-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="4f06c-123">**мултиплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="4f06c-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="4f06c-124">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="4f06c-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="4f06c-125">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="4f06c-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="4f06c-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="4f06c-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="4f06c-127">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4f06c-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
