---
description: Проверяет BoundingBox для пересечения с другим объектом.
ms.assetid: df3d3df9-aa74-413d-808c-f7b276d11279
title: BoundingBox. intersects, методы
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9039d99640ae3989d0b20e9d48f681edabb021f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544178"
---
# <a name="boundingboxintersects-methods"></a><span data-ttu-id="d8c37-103">BoundingBox. intersects, методы</span><span class="sxs-lookup"><span data-stu-id="d8c37-103">BoundingBox.Intersects methods</span></span>

<span data-ttu-id="d8c37-104">Проверяет BoundingBox для пересечения с другим объектом.</span><span class="sxs-lookup"><span data-stu-id="d8c37-104">Tests the BoundingBox for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d8c37-105">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="d8c37-105">Overload list</span></span>



| <span data-ttu-id="d8c37-106">Метод</span><span class="sxs-lookup"><span data-stu-id="d8c37-106">Method</span></span>                                                                                   | <span data-ttu-id="d8c37-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d8c37-107">Description</span></span>                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c37-108">[**BoundingBox:: intersects (КСМВЕКТОР)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="d8c37-108">[**BoundingBox::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span></span>                   | <span data-ttu-id="d8c37-109">Протестируйте BoundingBox для пересечения с плоскостью.</span><span class="sxs-lookup"><span data-stu-id="d8c37-109">Test the BoundingBox for intersection with a plane.</span></span><br/>                                                                     |
| <span data-ttu-id="d8c37-110">[**BoundingBox:: intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="d8c37-110">[**BoundingBox::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="d8c37-111">Проверяет BoundingBox для пересечения с другим BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="d8c37-111">Tests the BoundingBox for intersection with another BoundingBox.</span></span><br/>                                                        |
| <span data-ttu-id="d8c37-112">[**BoundingBox:: intersects (const Баундингсфере&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8c37-112">[**BoundingBox::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span></span>      | <span data-ttu-id="d8c37-113">Проверяет BoundingBox для пересечения с Баундингсфере.</span><span class="sxs-lookup"><span data-stu-id="d8c37-113">Tests the BoundingBox for intersection with a BoundingSphere.</span></span><br/>                                                           |
| <span data-ttu-id="d8c37-114">[**BoundingBox:: intersects (const Баундингфрустум&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="d8c37-114">[**BoundingBox::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="d8c37-115">Протестируйте [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) для пересечения с [**баундингфрустум**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span><span class="sxs-lookup"><span data-stu-id="d8c37-115">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="d8c37-116">[**BoundingBox:: intersects (КСМВЕКТОР, КСМВЕКТОР, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="d8c37-116">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="d8c37-117">Протестируйте BoundingBox для пересечения с лучом.</span><span class="sxs-lookup"><span data-stu-id="d8c37-117">Test the BoundingBox for intersection with a ray.</span></span><br/>                                                                       |
| <span data-ttu-id="d8c37-118">[**BoundingBox:: intersects (КСМВЕКТОР, КСМВЕКТОР, КСМВЕКТОР)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="d8c37-118">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="d8c37-119">Протестируйте BoundingBox для пересечения с треугольником.</span><span class="sxs-lookup"><span data-stu-id="d8c37-119">Test the BoundingBox for intersection with a triangle.</span></span><br/>                                                                  |
| <span data-ttu-id="d8c37-120">[**BoundingBox:: intersects (const Баундингориентедбокс&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="d8c37-120">[**BoundingBox::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="d8c37-121">Протестируйте [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) для пересечения с [**баундингориентедбокс**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="d8c37-121">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8c37-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d8c37-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c37-123">Методы</span><span class="sxs-lookup"><span data-stu-id="d8c37-123">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="d8c37-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d8c37-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8c37-125">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="d8c37-125">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
