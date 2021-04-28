---
description: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h) — загружает удостоверение в текущую матрицу.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107992"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="4ad5e-103">Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="4ad5e-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="4ad5e-104">Загружает удостоверение в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad5e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ad5e-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="4ad5e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ad5e-106">Parameters</span></span>

<span data-ttu-id="4ad5e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ad5e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ad5e-108">Return value</span></span>

<span data-ttu-id="4ad5e-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ad5e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ad5e-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4ad5e-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad5e-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="4ad5e-112">Remarks</span></span>

<span data-ttu-id="4ad5e-113">Матрица идентификаторов — это матрица, в которой все коэффициенты составляют 0,0, за исключением \[ коэффициентов 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4 и 4 \] , для которых задано значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="4ad5e-114">Матрица идентификации является особой в том, что при применении к вершинам они не меняются.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="4ad5e-115">Матрица идентификаторов используется в качестве начальной точки для матриц, которые будут изменять значения вершин для создания поворотов, переводов и других преобразований, которые могут быть представлены матрицей 4x4.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad5e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4ad5e-116">Requirements</span></span>



| <span data-ttu-id="4ad5e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4ad5e-117">Requirement</span></span> | <span data-ttu-id="4ad5e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4ad5e-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad5e-119">Header</span><span class="sxs-lookup"><span data-stu-id="4ad5e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4ad5e-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ad5e-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ad5e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ad5e-121">Library</span></span><br/> | <dl> <span data-ttu-id="4ad5e-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ad5e-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad5e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4ad5e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad5e-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="4ad5e-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="4ad5e-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="4ad5e-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




