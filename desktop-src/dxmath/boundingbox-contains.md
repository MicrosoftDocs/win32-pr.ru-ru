---
description: Проверяет, содержит ли BoundingBox указанный объект.
ms.assetid: 876c7764-9378-48e5-812c-3646930900c5
title: BoundingBox. Contains, методы
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 485dbbaf5ab4522eb50fe598325e5ecbb48fff57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544186"
---
# <a name="boundingboxcontains-methods"></a><span data-ttu-id="7b2d9-103">BoundingBox. Contains, методы</span><span class="sxs-lookup"><span data-stu-id="7b2d9-103">BoundingBox.Contains methods</span></span>

<span data-ttu-id="7b2d9-104">Проверяет, содержит ли BoundingBox указанный объект.</span><span class="sxs-lookup"><span data-stu-id="7b2d9-104">Tests whether the BoundingBox contains a specified object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7b2d9-105">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="7b2d9-105">Overload list</span></span>



| <span data-ttu-id="7b2d9-106">Метод</span><span class="sxs-lookup"><span data-stu-id="7b2d9-106">Method</span></span>                                                                               | <span data-ttu-id="7b2d9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2d9-107">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b2d9-108">**BoundingBox:: Contains (КСМВЕКТОР)**</span><span class="sxs-lookup"><span data-stu-id="7b2d9-108">**BoundingBox::Contains (XMVECTOR)**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains)                   | <span data-ttu-id="7b2d9-109">Проверяет, содержит ли BoundingBox указанную точку.</span><span class="sxs-lookup"><span data-stu-id="7b2d9-109">Tests the whether the BoundingBox contains a specified point.</span></span><br/>                                                                   |
| <span data-ttu-id="7b2d9-110">[**BoundingBox:: Contains (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="7b2d9-110">[**BoundingBox::Contains (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingbox_))</span></span>         | <span data-ttu-id="7b2d9-111">Проверяет, содержит ли BoundingBox другой BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="7b2d9-111">Tests whether the BoundingBox contains another BoundingBox.</span></span><br/>                                                                     |
| <span data-ttu-id="7b2d9-112">[**BoundingBox:: Contains (const Баундингсфере&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingsphere_))</span><span class="sxs-lookup"><span data-stu-id="7b2d9-112">[**BoundingBox::Contains (const BoundingSphere&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingsphere_))</span></span>      | <span data-ttu-id="7b2d9-113">Проверяет, содержит ли BoundingBox указанный Баундингсфере.</span><span class="sxs-lookup"><span data-stu-id="7b2d9-113">Tests whether the BoundingBox contains a specified BoundingSphere.</span></span><br/>                                                              |
| <span data-ttu-id="7b2d9-114">[**BoundingBox:: Contains (const Баундингфрустум&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="7b2d9-114">[**BoundingBox::Contains (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingfrustum_))</span></span>     | <span data-ttu-id="7b2d9-115">Проверяет, содержит ли [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) указанный [**баундингфрустум**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span><span class="sxs-lookup"><span data-stu-id="7b2d9-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contains the specified [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="7b2d9-116">[**BoundingBox:: Contains (КСМВЕКТОР, КСМВЕКТОР, КСМВЕКТОР)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="7b2d9-116">[**BoundingBox::Contains (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="7b2d9-117">Проверьте, содержит ли BoundingBox указанный треугольник.</span><span class="sxs-lookup"><span data-stu-id="7b2d9-117">Test whether the BoundingBox contains a specified triangle.</span></span><br/>                                                                     |
| <span data-ttu-id="7b2d9-118">[**BoundingBox:: Contains (const Баундингориентедбокс&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="7b2d9-118">[**BoundingBox::Contains (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingorientedbox_))</span></span> | <span data-ttu-id="7b2d9-119">Проверяет, содержит ли [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) указанный [**баундингориентедбокс**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="7b2d9-119">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contains the specified [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b2d9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7b2d9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2d9-121">Методы</span><span class="sxs-lookup"><span data-stu-id="7b2d9-121">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="7b2d9-122">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7b2d9-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7b2d9-123">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="7b2d9-123">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
