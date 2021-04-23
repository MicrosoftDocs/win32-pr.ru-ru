---
description: Определяет параметры для выполнения вычислений геодезические Distance при подсчете текстуры на изогнутую поверхность. Используйте этот флаг, чтобы выбрать между высоким качеством и быстрыми вычислениями при вычислении текстуры Atlas.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Перечисление D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713606"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="647b2-104">Перечисление D3DXUVATLAS</span><span class="sxs-lookup"><span data-stu-id="647b2-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="647b2-105">Определяет параметры для выполнения вычислений геодезические Distance при подсчете текстуры на изогнутую поверхность.</span><span class="sxs-lookup"><span data-stu-id="647b2-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="647b2-106">Используйте этот флаг, чтобы выбрать между высоким качеством и быстрыми вычислениями при вычислении текстуры Atlas.</span><span class="sxs-lookup"><span data-stu-id="647b2-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="647b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="647b2-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="647b2-108">Константы</span><span class="sxs-lookup"><span data-stu-id="647b2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="647b2-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="647b2-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="647b2-110">К сеткам с более чем 25kными лицами будет применяться метод жеодасик Distance, тогда как в сетках с числом лиц, меньшим, чем 25k, вместо них будет использоваться метод повышения качества геодезические.</span><span class="sxs-lookup"><span data-stu-id="647b2-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="647b2-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ геодезические \_ fast**</span><span class="sxs-lookup"><span data-stu-id="647b2-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="647b2-112">Использует приближения для повышения скорости построения диаграммы за счет увеличения или увеличения количества диаграмм, выводимых для сетки.</span><span class="sxs-lookup"><span data-stu-id="647b2-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="647b2-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS \_ геодезические \_ качество**</span><span class="sxs-lookup"><span data-stu-id="647b2-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="647b2-114">Обеспечивает более качественные диаграммы, но требует больше времени и памяти, чем быстро.</span><span class="sxs-lookup"><span data-stu-id="647b2-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="647b2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="647b2-115">Requirements</span></span>



| <span data-ttu-id="647b2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="647b2-116">Requirement</span></span> | <span data-ttu-id="647b2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="647b2-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="647b2-118">Header</span><span class="sxs-lookup"><span data-stu-id="647b2-118">Header</span></span><br/> | <dl> <span data-ttu-id="647b2-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="647b2-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="647b2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="647b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647b2-121">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="647b2-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




