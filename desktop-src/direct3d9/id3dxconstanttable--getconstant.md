---
description: Метод ID3DXConstantTable::-Constant — возвращает константу путем поиска своего индекса.
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: Метод ID3DXConstantTable::-Constant (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115272"
---
# <a name="id3dxconstanttablegetconstant-method"></a><span data-ttu-id="08ee1-103">Метод ID3DXConstantTable:: with Constant</span><span class="sxs-lookup"><span data-stu-id="08ee1-103">ID3DXConstantTable::GetConstant method</span></span>

<span data-ttu-id="08ee1-104">Возвращает константу путем поиска своего индекса.</span><span class="sxs-lookup"><span data-stu-id="08ee1-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ee1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08ee1-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="08ee1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08ee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ee1-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08ee1-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ee1-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="08ee1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="08ee1-109">Уникальный идентификатор родительской структуры данных.</span><span class="sxs-lookup"><span data-stu-id="08ee1-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="08ee1-110">Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="08ee1-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="08ee1-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08ee1-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ee1-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08ee1-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08ee1-113">Отсчитываемый от нуля индекс константы.</span><span class="sxs-lookup"><span data-stu-id="08ee1-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ee1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08ee1-114">Return value</span></span>

<span data-ttu-id="08ee1-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="08ee1-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="08ee1-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="08ee1-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="08ee1-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="08ee1-117">Remarks</span></span>

<span data-ttu-id="08ee1-118">Чтобы получить константу из массива констант, используйте [**ID3DXConstantTable:: жетконстантелемент**](id3dxconstanttable--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="08ee1-118">To get a constant from an array of constants, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08ee1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="08ee1-119">Requirements</span></span>



| <span data-ttu-id="08ee1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="08ee1-120">Requirement</span></span> | <span data-ttu-id="08ee1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="08ee1-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ee1-122">Header</span><span class="sxs-lookup"><span data-stu-id="08ee1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="08ee1-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="08ee1-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="08ee1-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="08ee1-124">Library</span></span><br/> | <dl> <span data-ttu-id="08ee1-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08ee1-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08ee1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="08ee1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ee1-127">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="08ee1-127">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
