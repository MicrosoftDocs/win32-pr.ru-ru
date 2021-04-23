---
description: Задает координаты шаг текселя барицентрик.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'Метод ID3DXTextureGutterHelper:: Сетбаримап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273922"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="28c4d-103">Метод ID3DXTextureGutterHelper:: Сетбаримап</span><span class="sxs-lookup"><span data-stu-id="28c4d-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="28c4d-104">Задает координаты шаг текселя барицентрик.</span><span class="sxs-lookup"><span data-stu-id="28c4d-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28c4d-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="28c4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28c4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c4d-107">*пбаридата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="28c4d-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="28c4d-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , содержащую первые две координаты барицентрик каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="28c4d-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c4d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28c4d-110">Return value</span></span>

<span data-ttu-id="28c4d-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28c4d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28c4d-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="28c4d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="28c4d-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="28c4d-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="28c4d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28c4d-114">Remarks</span></span>

<span data-ttu-id="28c4d-115">Третья координата барицентрик предоставляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28c4d-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="28c4d-116">Входные координаты барицентрик для этого метода допустимы только для допустимых пикселей текстуры (не являющихся классами 0).</span><span class="sxs-lookup"><span data-stu-id="28c4d-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="28c4d-117">[**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="28c4d-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="28c4d-118">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="28c4d-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="28c4d-119">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="28c4d-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="28c4d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="28c4d-120">Requirements</span></span>



| <span data-ttu-id="28c4d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="28c4d-121">Requirement</span></span> | <span data-ttu-id="28c4d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="28c4d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c4d-123">Header</span><span class="sxs-lookup"><span data-stu-id="28c4d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="28c4d-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c4d-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="28c4d-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28c4d-125">Library</span></span><br/> | <dl> <span data-ttu-id="28c4d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28c4d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28c4d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28c4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c4d-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="28c4d-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




