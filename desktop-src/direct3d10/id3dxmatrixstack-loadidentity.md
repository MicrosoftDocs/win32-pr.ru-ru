---
description: Загружает удостоверение в текущую матрицу.
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
ms.openlocfilehash: 85a58529be3bfcb4d52ba096bb6134fe08994d77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714022"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="d339d-103">Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d339d-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="d339d-104">Загружает удостоверение в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="d339d-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d339d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d339d-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="d339d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d339d-106">Parameters</span></span>

<span data-ttu-id="d339d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d339d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d339d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d339d-108">Return value</span></span>

<span data-ttu-id="d339d-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d339d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d339d-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d339d-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d339d-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d339d-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d339d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d339d-112">Remarks</span></span>

<span data-ttu-id="d339d-113">Матрица идентификаторов — это матрица, в которой все коэффициенты составляют 0,0, за исключением \[ коэффициентов 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4 и 4 \] , для которых задано значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="d339d-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="d339d-114">Матрица идентификации является особой в том, что при применении к вершинам они не меняются.</span><span class="sxs-lookup"><span data-stu-id="d339d-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="d339d-115">Матрица идентификаторов используется в качестве начальной точки для матриц, которые будут изменять значения вершин для создания поворотов, переводов и других преобразований, которые могут быть представлены матрицей 4x4.</span><span class="sxs-lookup"><span data-stu-id="d339d-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d339d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d339d-116">Requirements</span></span>



| <span data-ttu-id="d339d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d339d-117">Requirement</span></span> | <span data-ttu-id="d339d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d339d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d339d-119">Header</span><span class="sxs-lookup"><span data-stu-id="d339d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d339d-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d339d-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d339d-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d339d-121">Library</span></span><br/> | <dl> <span data-ttu-id="d339d-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d339d-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d339d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d339d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d339d-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d339d-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d339d-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="d339d-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




