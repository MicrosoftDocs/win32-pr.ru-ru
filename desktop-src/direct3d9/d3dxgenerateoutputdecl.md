---
description: Создает объявление вершины вывода из объявления ввода. Объявление вывода предназначено для использования функциями тесселяции сетки.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Функция D3DXGenerateOutputDecl (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713680"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="351ce-104">Функция D3DXGenerateOutputDecl</span><span class="sxs-lookup"><span data-stu-id="351ce-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="351ce-105">Создает объявление вершины вывода из объявления ввода.</span><span class="sxs-lookup"><span data-stu-id="351ce-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="351ce-106">Объявление вывода предназначено для использования функциями тесселяции сетки.</span><span class="sxs-lookup"><span data-stu-id="351ce-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="351ce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="351ce-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="351ce-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="351ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="351ce-109">*паутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="351ce-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="351ce-110">Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="351ce-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="351ce-111">Указатель на объявление выходной вершины.</span><span class="sxs-lookup"><span data-stu-id="351ce-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="351ce-112">См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="351ce-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="351ce-113">*пинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="351ce-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351ce-114">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="351ce-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="351ce-115">Указатель на объявление входного вершины.</span><span class="sxs-lookup"><span data-stu-id="351ce-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="351ce-116">См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="351ce-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="351ce-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="351ce-117">Return value</span></span>

<span data-ttu-id="351ce-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="351ce-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="351ce-119">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="351ce-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="351ce-120">Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="351ce-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="351ce-121">Требования</span><span class="sxs-lookup"><span data-stu-id="351ce-121">Requirements</span></span>



| <span data-ttu-id="351ce-122">Требование</span><span class="sxs-lookup"><span data-stu-id="351ce-122">Requirement</span></span> | <span data-ttu-id="351ce-123">Значение</span><span class="sxs-lookup"><span data-stu-id="351ce-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="351ce-124">Header</span><span class="sxs-lookup"><span data-stu-id="351ce-124">Header</span></span><br/>  | <dl> <span data-ttu-id="351ce-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="351ce-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="351ce-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="351ce-126">Library</span></span><br/> | <dl> <span data-ttu-id="351ce-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="351ce-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="351ce-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="351ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="351ce-129">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="351ce-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




