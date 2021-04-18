---
description: Рисует подмножество сетки.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: 'ID3DX10Mesh: метод:D Равсубсет (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674699"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="b4ef5-103">ID3DX10Mesh: метод:D Равсубсет</span><span class="sxs-lookup"><span data-stu-id="b4ef5-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="b4ef5-104">Рисует подмножество сетки.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ef5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4ef5-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="b4ef5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4ef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ef5-107">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4ef5-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ef5-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ef5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4ef5-109">Указывает подмножество рисуемой сетки.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="b4ef5-110">Это значение используется для различения лиц в сетке как принадлежащих одной или нескольким группам атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4ef5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4ef5-111">Return value</span></span>

<span data-ttu-id="b4ef5-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4ef5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4ef5-113">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b4ef5-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ef5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4ef5-114">Remarks</span></span>

<span data-ttu-id="b4ef5-115">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="b4ef5-116">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ef5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b4ef5-117">Requirements</span></span>



| <span data-ttu-id="b4ef5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b4ef5-118">Requirement</span></span> | <span data-ttu-id="b4ef5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b4ef5-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ef5-120">Header</span><span class="sxs-lookup"><span data-stu-id="b4ef5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b4ef5-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ef5-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4ef5-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4ef5-122">Library</span></span><br/> | <dl> <span data-ttu-id="b4ef5-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4ef5-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ef5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4ef5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ef5-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="b4ef5-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="b4ef5-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="b4ef5-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
