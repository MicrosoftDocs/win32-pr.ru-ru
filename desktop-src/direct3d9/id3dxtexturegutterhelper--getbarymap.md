---
description: Получает координаты шаг текселя барицентрик.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'Метод ID3DXTextureGutterHelper:: Жетбаримап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703856"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="182a9-103">Метод ID3DXTextureGutterHelper:: Жетбаримап</span><span class="sxs-lookup"><span data-stu-id="182a9-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="182a9-104">Получает координаты шаг текселя барицентрик.</span><span class="sxs-lookup"><span data-stu-id="182a9-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="182a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="182a9-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="182a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="182a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182a9-107">*пбаридата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="182a9-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="182a9-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="182a9-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="182a9-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , содержащую первые две координаты барицентрик каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="182a9-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182a9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="182a9-110">Return value</span></span>

<span data-ttu-id="182a9-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="182a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="182a9-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="182a9-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="182a9-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="182a9-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="182a9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="182a9-114">Remarks</span></span>

<span data-ttu-id="182a9-115">Третья координата барицентрик предоставляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="182a9-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="182a9-116">Координаты барицентрик всегда указываются по отношению к треугольнику, возвращенному [**ID3DXTextureGutterHelper:: жетфацемап**](id3dxtexturegutterhelper--getfacemap.md).</span><span class="sxs-lookup"><span data-stu-id="182a9-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="182a9-117">Координаты барицентрик, возвращаемые этим методом, допустимы только для допустимых пикселей текстуры (не являющихся классами 0).</span><span class="sxs-lookup"><span data-stu-id="182a9-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="182a9-118">[**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="182a9-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="182a9-119">[**Класс 2 пикселей текстуры**](id3dxtexturegutterhelper.md) сопоставляются с ближайшей точкой треугольника в шаг текселя пространстве.</span><span class="sxs-lookup"><span data-stu-id="182a9-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="182a9-120">Приложение должно выделить Пбаридата и управлять им.</span><span class="sxs-lookup"><span data-stu-id="182a9-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="182a9-121">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="182a9-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="182a9-122">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="182a9-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="182a9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="182a9-123">Requirements</span></span>



| <span data-ttu-id="182a9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="182a9-124">Requirement</span></span> | <span data-ttu-id="182a9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="182a9-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="182a9-126">Header</span><span class="sxs-lookup"><span data-stu-id="182a9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="182a9-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="182a9-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="182a9-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="182a9-128">Library</span></span><br/> | <dl> <span data-ttu-id="182a9-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="182a9-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="182a9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="182a9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182a9-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="182a9-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




