---
description: Рисует полосу линий в пространстве экрана. Входные данные указываются в виде массива, определяющего точки (Of D3DXVECTOR2) на полосе строк.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine::D необработанный метод (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694284"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="6323f-104">ID3DXLine::D необработанный метод</span><span class="sxs-lookup"><span data-stu-id="6323f-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="6323f-105">Рисует полосу линий в пространстве экрана.</span><span class="sxs-lookup"><span data-stu-id="6323f-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="6323f-106">Входные данные указываются в виде массива, определяющего точки (of [**D3DXVECTOR2**](d3dxvector2.md)) на полосе строк.</span><span class="sxs-lookup"><span data-stu-id="6323f-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="6323f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6323f-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="6323f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6323f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6323f-109">*пвертекслист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6323f-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6323f-110">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6323f-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6323f-111">Массив вершин, образующих линию.</span><span class="sxs-lookup"><span data-stu-id="6323f-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="6323f-112">См. [**D3DXVECTOR2**](d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="6323f-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="6323f-113">*дввертекслисткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6323f-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6323f-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6323f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6323f-115">Число вершин в списке вершин.</span><span class="sxs-lookup"><span data-stu-id="6323f-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="6323f-116">*Цветовая палитра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6323f-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6323f-117">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="6323f-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="6323f-118">Цвет линии.</span><span class="sxs-lookup"><span data-stu-id="6323f-118">Color of the line.</span></span> <span data-ttu-id="6323f-119">См. [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="6323f-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6323f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6323f-120">Return value</span></span>

<span data-ttu-id="6323f-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6323f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6323f-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6323f-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6323f-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6323f-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="6323f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6323f-124">Requirements</span></span>



| <span data-ttu-id="6323f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6323f-125">Requirement</span></span> | <span data-ttu-id="6323f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6323f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6323f-127">Header</span><span class="sxs-lookup"><span data-stu-id="6323f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6323f-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6323f-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6323f-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6323f-129">Library</span></span><br/> | <dl> <span data-ttu-id="6323f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6323f-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6323f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6323f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6323f-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="6323f-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
