---
description: Загружает удостоверение в текущую матрицу.
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e7ebc7b61679dc3938c2a57aa2346a45b136e5a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713556"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="0e720-103">Метод ID3DXMATRIXStack:: Лоадидентити (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0e720-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="0e720-104">Загружает удостоверение в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="0e720-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e720-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e720-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="0e720-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e720-106">Parameters</span></span>

<span data-ttu-id="0e720-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0e720-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e720-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e720-108">Return value</span></span>

<span data-ttu-id="0e720-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e720-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e720-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0e720-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e720-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0e720-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e720-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e720-112">Remarks</span></span>

<span data-ttu-id="0e720-113">Матрица идентификаторов — это матрица, в которой все коэффициенты составляют 0,0, за исключением \[ коэффициентов 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4 и 4 \] , для которых задано значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="0e720-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="0e720-114">Матрица идентификации является особой в том, что при применении к вершинам они не меняются.</span><span class="sxs-lookup"><span data-stu-id="0e720-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="0e720-115">Матрица идентификаторов используется в качестве начальной точки для матриц, которые будут изменять значения вершин для создания поворотов, переводов и других преобразований, которые могут быть представлены матрицей 4x4.</span><span class="sxs-lookup"><span data-stu-id="0e720-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e720-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0e720-116">Requirements</span></span>



| <span data-ttu-id="0e720-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0e720-117">Requirement</span></span> | <span data-ttu-id="0e720-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0e720-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e720-119">Header</span><span class="sxs-lookup"><span data-stu-id="0e720-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0e720-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e720-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0e720-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e720-121">Library</span></span><br/> | <dl> <span data-ttu-id="0e720-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e720-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e720-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e720-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e720-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="0e720-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0e720-125">**ID3DXMATRIXStack:: Лоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="0e720-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




