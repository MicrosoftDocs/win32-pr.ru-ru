---
description: Возвращает декларатор из кода гибкого формата вершины (ФВФ).
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: Функция D3DXDeclaratorFromFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703794"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="95e91-103">Функция D3DXDeclaratorFromFVF</span><span class="sxs-lookup"><span data-stu-id="95e91-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="95e91-104">Возвращает декларатор из кода гибкого формата вершины (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="95e91-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95e91-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="95e91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95e91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e91-107">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95e91-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e91-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e91-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e91-109">Сочетание [D3DFVF](d3dfvf.md) , которое описывает фвф, из которого создается возвращаемый массив декларатора.</span><span class="sxs-lookup"><span data-stu-id="95e91-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="95e91-110">*Объявление* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="95e91-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95e91-111">Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="95e91-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="95e91-112">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершин вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="95e91-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="95e91-113">Верхний предел этого массива декларатора — [**Max \_ фвф \_ DECL \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="95e91-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e91-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95e91-114">Return value</span></span>

<span data-ttu-id="95e91-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95e91-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95e91-116">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="95e91-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95e91-117">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DXERR \_ инвалидмеш.</span><span class="sxs-lookup"><span data-stu-id="95e91-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e91-118">Требования</span><span class="sxs-lookup"><span data-stu-id="95e91-118">Requirements</span></span>



| <span data-ttu-id="95e91-119">Требование</span><span class="sxs-lookup"><span data-stu-id="95e91-119">Requirement</span></span> | <span data-ttu-id="95e91-120">Значение</span><span class="sxs-lookup"><span data-stu-id="95e91-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95e91-121">Header</span><span class="sxs-lookup"><span data-stu-id="95e91-121">Header</span></span><br/>  | <dl> <span data-ttu-id="95e91-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e91-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="95e91-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95e91-123">Library</span></span><br/> | <dl> <span data-ttu-id="95e91-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95e91-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95e91-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95e91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e91-126">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="95e91-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="95e91-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="95e91-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
