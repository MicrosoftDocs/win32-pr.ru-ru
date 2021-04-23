---
description: Определяет флаги, используемые для управления числом или матрицами, применяемыми системой при выполнении многоматричного смешения вершин.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Перечисление D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354733"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="1f066-103">Перечисление D3DVERTEXBLENDFLAGS</span><span class="sxs-lookup"><span data-stu-id="1f066-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="1f066-104">Определяет флаги, используемые для управления числом или матрицами, применяемыми системой при выполнении многоматричного смешения вершин.</span><span class="sxs-lookup"><span data-stu-id="1f066-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f066-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f066-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="1f066-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1f066-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f066-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**\_Отключение D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="1f066-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="1f066-108">Отключить смешение вершин; Примените только матрицу World, заданную с помощью макроса [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояния преобразования равно 0.</span><span class="sxs-lookup"><span data-stu-id="1f066-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="1f066-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="1f066-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="1f066-110">Включите смешение вершин между двумя матрицами, заданными в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояний преобразования — 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="1f066-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="1f066-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="1f066-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="1f066-112">Включите смешение вершин между тремя матрицами, заданными в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояний преобразования — 0, 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="1f066-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="1f066-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="1f066-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="1f066-114">Включите смешение вершин между четырьмя матрицами, заданными в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояний преобразования — 0, 1, 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="1f066-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="1f066-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**Tween — D3DVBF \_**</span><span class="sxs-lookup"><span data-stu-id="1f066-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="1f066-116">Смешивание вершин выполняется с использованием значения, присвоенного D3DRS \_ твинфактор.</span><span class="sxs-lookup"><span data-stu-id="1f066-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="1f066-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="1f066-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="1f066-118">Используйте одну матрицу с весом 1,0.</span><span class="sxs-lookup"><span data-stu-id="1f066-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f066-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f066-119">Remarks</span></span>

<span data-ttu-id="1f066-120">Члены этого типа используются с \_ состоянием отрисовки D3DRS вертексбленд.</span><span class="sxs-lookup"><span data-stu-id="1f066-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="1f066-121">Смешивание геометрических объектов (многоматричное смешение вершин) требует, чтобы приложение использовало формат вершин, в котором для каждой вершины используются веса смешения (бета-версии).</span><span class="sxs-lookup"><span data-stu-id="1f066-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f066-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1f066-122">Requirements</span></span>



| <span data-ttu-id="1f066-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1f066-123">Requirement</span></span> | <span data-ttu-id="1f066-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1f066-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f066-125">Header</span><span class="sxs-lookup"><span data-stu-id="1f066-125">Header</span></span><br/> | <dl> <span data-ttu-id="1f066-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f066-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f066-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f066-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f066-128">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="1f066-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1f066-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="1f066-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="1f066-130">**D3DTS \_ мир**</span><span class="sxs-lookup"><span data-stu-id="1f066-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="1f066-131">**D3DTS \_ ворлдн**</span><span class="sxs-lookup"><span data-stu-id="1f066-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="1f066-132">**D3DTS \_ ворлдматрикс**</span><span class="sxs-lookup"><span data-stu-id="1f066-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
