---
description: Рисует полосу линий в пространстве экрана с заданной матрицей преобразования входных данных.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: 'ID3DXLine: метод:D Равтрансформ (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694283"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="0be59-103">ID3DXLine: метод:D Равтрансформ</span><span class="sxs-lookup"><span data-stu-id="0be59-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="0be59-104">Рисует полосу линий в пространстве экрана с заданной матрицей преобразования входных данных.</span><span class="sxs-lookup"><span data-stu-id="0be59-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0be59-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="0be59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0be59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be59-107">*пвертекслист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be59-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be59-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be59-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0be59-109">Массив вершин, образующих линию.</span><span class="sxs-lookup"><span data-stu-id="0be59-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="0be59-110">См. [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="0be59-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="0be59-111">*дввертекслисткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be59-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be59-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0be59-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0be59-113">Число вершин в списке вершин.</span><span class="sxs-lookup"><span data-stu-id="0be59-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="0be59-114">*птрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be59-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be59-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be59-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0be59-116">Матрица масштабирования, вращения и сдвига (SRT) для преобразования точек.</span><span class="sxs-lookup"><span data-stu-id="0be59-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="0be59-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0be59-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="0be59-118">Если эта матрица является матрицей проекции, то все стипплед линии будут отображаться с шаблоном стипплинг с перспективой.</span><span class="sxs-lookup"><span data-stu-id="0be59-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="0be59-119">Также можно преобразовать вершины и использовать [**ID3DXLine::D RAW**](id3dxline--draw.md) , чтобы нарисовать линию с неправильным шаблоном стиппле.</span><span class="sxs-lookup"><span data-stu-id="0be59-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="0be59-120">*Цветовая палитра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be59-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be59-121">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="0be59-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="0be59-122">Цвет линии.</span><span class="sxs-lookup"><span data-stu-id="0be59-122">Color of the line.</span></span> <span data-ttu-id="0be59-123">См. [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="0be59-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be59-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0be59-124">Return value</span></span>

<span data-ttu-id="0be59-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0be59-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0be59-126">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0be59-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0be59-127">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0be59-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be59-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0be59-128">Requirements</span></span>



| <span data-ttu-id="0be59-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0be59-129">Requirement</span></span> | <span data-ttu-id="0be59-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0be59-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0be59-131">Header</span><span class="sxs-lookup"><span data-stu-id="0be59-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0be59-132"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be59-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0be59-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0be59-133">Library</span></span><br/> | <dl> <span data-ttu-id="0be59-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0be59-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0be59-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0be59-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be59-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="0be59-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
