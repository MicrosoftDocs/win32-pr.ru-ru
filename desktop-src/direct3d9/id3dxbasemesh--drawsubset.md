---
description: 'ID3DXBaseMesh: метод:D Равсубсет — рисует подмножество сетки.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: 'ID3DXBaseMesh: метод:D Равсубсет (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115472"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="104a7-103">ID3DXBaseMesh: метод:D Равсубсет</span><span class="sxs-lookup"><span data-stu-id="104a7-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="104a7-104">Рисует подмножество сетки.</span><span class="sxs-lookup"><span data-stu-id="104a7-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="104a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="104a7-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="104a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="104a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104a7-107">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="104a7-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104a7-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="104a7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="104a7-109">Значение типа DWORD, указывающее подмножество рисуемой сетки.</span><span class="sxs-lookup"><span data-stu-id="104a7-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="104a7-110">Это значение используется для различения лиц в сетке как принадлежащих одной или нескольким группам атрибутов.</span><span class="sxs-lookup"><span data-stu-id="104a7-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104a7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="104a7-111">Return value</span></span>

<span data-ttu-id="104a7-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="104a7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="104a7-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="104a7-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="104a7-114">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="104a7-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="104a7-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="104a7-115">Remarks</span></span>

<span data-ttu-id="104a7-116">Подмножество, заданное Аттрибид, будет подготовлено к просмотру с помощью метода [**IDirect3DDevice9::D равиндекседпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) , используя \_ тип-примитив D3DPT трианглелист, поэтому буфер индекса должен быть правильно инициализирован.</span><span class="sxs-lookup"><span data-stu-id="104a7-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="104a7-117">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="104a7-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="104a7-118">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (*аттрибид*) при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="104a7-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="104a7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="104a7-119">Requirements</span></span>



| <span data-ttu-id="104a7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="104a7-120">Requirement</span></span> | <span data-ttu-id="104a7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="104a7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="104a7-122">Header</span><span class="sxs-lookup"><span data-stu-id="104a7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="104a7-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="104a7-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="104a7-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="104a7-124">Library</span></span><br/> | <dl> <span data-ttu-id="104a7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="104a7-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="104a7-126">См. также</span><span class="sxs-lookup"><span data-stu-id="104a7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104a7-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="104a7-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
