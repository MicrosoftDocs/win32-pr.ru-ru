---
description: Возвращает константу из массива констант. Массив состоит из элементов.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'Метод ID3DXConstantTable:: Жетконстантелемент (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713736"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="29a8d-104">Метод ID3DXConstantTable:: Жетконстантелемент</span><span class="sxs-lookup"><span data-stu-id="29a8d-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="29a8d-105">Возвращает константу из массива констант.</span><span class="sxs-lookup"><span data-stu-id="29a8d-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="29a8d-106">Массив состоит из элементов.</span><span class="sxs-lookup"><span data-stu-id="29a8d-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a8d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29a8d-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="29a8d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="29a8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29a8d-109">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29a8d-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29a8d-110">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="29a8d-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="29a8d-111">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="29a8d-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="29a8d-112">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="29a8d-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="29a8d-113">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29a8d-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29a8d-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29a8d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29a8d-115">Отсчитываемый от нуля индекс элемента в массиве.</span><span class="sxs-lookup"><span data-stu-id="29a8d-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29a8d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29a8d-116">Return value</span></span>

<span data-ttu-id="29a8d-117">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="29a8d-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="29a8d-118">Возвращает уникальный идентификатор для константы элемента.</span><span class="sxs-lookup"><span data-stu-id="29a8d-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="29a8d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29a8d-119">Remarks</span></span>

<span data-ttu-id="29a8d-120">Чтобы получить константу, которая не является частью массива, используйте [**ID3DXConstantTable::-Constant**](id3dxconstanttable--getconstant.md) или [**ID3DXConstantTable:: жетконстантбинаме**](id3dxconstanttable--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="29a8d-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29a8d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="29a8d-121">Requirements</span></span>



| <span data-ttu-id="29a8d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="29a8d-122">Requirement</span></span> | <span data-ttu-id="29a8d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="29a8d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a8d-124">Header</span><span class="sxs-lookup"><span data-stu-id="29a8d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="29a8d-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="29a8d-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="29a8d-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="29a8d-126">Library</span></span><br/> | <dl> <span data-ttu-id="29a8d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29a8d-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="29a8d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29a8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a8d-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="29a8d-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
