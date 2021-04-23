---
description: Добавляет смежные данные в буфер индекса сетки. Когда сеть должна быть отправлена в шейдер Geometry, который принимает данные из соседей по смежным связям, необходимо, чтобы буфер индексов сетки содержал смежные данные.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'Метод ID3DX10Mesh:: Женератегсаджаценци (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081898"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="1a33c-104">Метод ID3DX10Mesh:: Женератегсаджаценци</span><span class="sxs-lookup"><span data-stu-id="1a33c-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="1a33c-105">Добавляет смежные данные в буфер индекса сетки.</span><span class="sxs-lookup"><span data-stu-id="1a33c-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="1a33c-106">Когда сеть должна быть отправлена в шейдер Geometry, который принимает данные из соседей по смежным связям, необходимо, чтобы буфер индексов сетки содержал смежные данные.</span><span class="sxs-lookup"><span data-stu-id="1a33c-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a33c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a33c-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="1a33c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a33c-108">Parameters</span></span>

<span data-ttu-id="1a33c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1a33c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a33c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a33c-110">Return value</span></span>

<span data-ttu-id="1a33c-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a33c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a33c-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a33c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1a33c-113">Requirements</span></span>



| <span data-ttu-id="1a33c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1a33c-114">Requirement</span></span> | <span data-ttu-id="1a33c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1a33c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a33c-116">Header</span><span class="sxs-lookup"><span data-stu-id="1a33c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1a33c-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a33c-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a33c-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a33c-118">Library</span></span><br/> | <dl> <span data-ttu-id="1a33c-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a33c-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a33c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a33c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a33c-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="1a33c-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="1a33c-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="1a33c-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




