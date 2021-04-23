---
description: Возвращает код гибкого формата вершины (ФВФ) из декларатора.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: Функция D3DXFVFFromDeclarator (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354840"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="4a873-103">Функция D3DXFVFFromDeclarator</span><span class="sxs-lookup"><span data-stu-id="4a873-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="4a873-104">Возвращает код гибкого формата вершины (ФВФ) из декларатора.</span><span class="sxs-lookup"><span data-stu-id="4a873-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a873-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a873-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="4a873-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a873-107">*пдекларатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a873-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a873-108">Тип: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a873-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4a873-109">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , ОПИСЫВАЮЩИХ код фвф.</span><span class="sxs-lookup"><span data-stu-id="4a873-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="4a873-110">*пфвф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4a873-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a873-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a873-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4a873-112">Указатель на значение DWORD, представляющее возвращаемое сочетание [D3DFVF](d3dfvf.md) , которое описывает формат вершин, возвращенный методом декларатора.</span><span class="sxs-lookup"><span data-stu-id="4a873-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a873-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a873-113">Return value</span></span>

<span data-ttu-id="4a873-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a873-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a873-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4a873-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4a873-116">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4a873-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a873-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a873-117">Remarks</span></span>

<span data-ttu-id="4a873-118">Эта функция завершится ошибкой для любого декларатора, который не сопоставлен непосредственно с ФВФ.</span><span class="sxs-lookup"><span data-stu-id="4a873-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a873-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4a873-119">Requirements</span></span>



| <span data-ttu-id="4a873-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4a873-120">Requirement</span></span> | <span data-ttu-id="4a873-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4a873-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a873-122">Header</span><span class="sxs-lookup"><span data-stu-id="4a873-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4a873-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a873-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4a873-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a873-124">Library</span></span><br/> | <dl> <span data-ttu-id="4a873-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a873-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a873-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a873-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a873-127">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="4a873-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="4a873-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="4a873-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
