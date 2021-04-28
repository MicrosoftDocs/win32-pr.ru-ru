---
description: 'Метод ID3DXConstantTable:: Жетконстантбинаме — возвращает константу путем поиска ее имени.'
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'Метод ID3DXConstantTable:: Жетконстантбинаме (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88461a45bf484a72c085f1776eb923a8534b8be3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115252"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="5f3f4-103">Метод ID3DXConstantTable:: Жетконстантбинаме</span><span class="sxs-lookup"><span data-stu-id="5f3f4-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="5f3f4-104">Возвращает константу путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="5f3f4-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f3f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f3f4-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="5f3f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f3f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f3f4-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f3f4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f3f4-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5f3f4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5f3f4-109">Уникальный идентификатор родительской структуры данных.</span><span class="sxs-lookup"><span data-stu-id="5f3f4-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="5f3f4-110">Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f3f4-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5f3f4-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f3f4-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f3f4-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f3f4-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f3f4-113">Имя константы.</span><span class="sxs-lookup"><span data-stu-id="5f3f4-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f3f4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f3f4-114">Return value</span></span>

<span data-ttu-id="5f3f4-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5f3f4-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5f3f4-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="5f3f4-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f3f4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5f3f4-117">Requirements</span></span>



| <span data-ttu-id="5f3f4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5f3f4-118">Requirement</span></span> | <span data-ttu-id="5f3f4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5f3f4-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f3f4-120">Header</span><span class="sxs-lookup"><span data-stu-id="5f3f4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5f3f4-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f3f4-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5f3f4-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f3f4-122">Library</span></span><br/> | <dl> <span data-ttu-id="5f3f4-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f3f4-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5f3f4-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5f3f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f3f4-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5f3f4-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
