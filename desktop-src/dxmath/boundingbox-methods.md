---
description: Методы BoundingBox
ms.assetid: 68db5936-f0f8-4dbd-a183-b6c3089af0f0
title: Методы BoundingBox
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b58c79f202304a289bf1e30447b76ba9ad6dc83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711548"
---
# <a name="boundingbox-methods"></a><span data-ttu-id="a9970-103">Методы BoundingBox</span><span class="sxs-lookup"><span data-stu-id="a9970-103">BoundingBox Methods</span></span>



| <span data-ttu-id="a9970-104">Метод</span><span class="sxs-lookup"><span data-stu-id="a9970-104">Method</span></span>                                                              | <span data-ttu-id="a9970-105">Описание</span><span class="sxs-lookup"><span data-stu-id="a9970-105">Description</span></span>                                                                                            |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9970-106">**Содержащих**</span><span class="sxs-lookup"><span data-stu-id="a9970-106">**Contains**</span></span>](boundingbox-contains.md)<br/>                 | <span data-ttu-id="a9970-107">Проверяет, содержит ли BoundingBox указанный объект.</span><span class="sxs-lookup"><span data-stu-id="a9970-107">Tests whether the BoundingBox contains a specified object.</span></span><br/>                                  |
| [<span data-ttu-id="a9970-108">**креатефромпоинтс**</span><span class="sxs-lookup"><span data-stu-id="a9970-108">**CreateFromPoints**</span></span>](boundingbox-createfrompoints.md)<br/> | <span data-ttu-id="a9970-109">Создает BoundingBox из точек.</span><span class="sxs-lookup"><span data-stu-id="a9970-109">Creates a BoundingBox from points.</span></span><br/>                                                          |
| [<span data-ttu-id="a9970-110">**Пересекает**</span><span class="sxs-lookup"><span data-stu-id="a9970-110">**Intersects**</span></span>](boundingbox-intersects.md)<br/>             | <span data-ttu-id="a9970-111">Проверяет BoundingBox для пересечения с другим объектом.</span><span class="sxs-lookup"><span data-stu-id="a9970-111">Tests the BoundingBox for intersection with another object.</span></span><br/>                                 |
| [<span data-ttu-id="a9970-112">**Преобразование**</span><span class="sxs-lookup"><span data-stu-id="a9970-112">**Transform**</span></span>](boundingbox-transform.md)<br/>               | <span data-ttu-id="a9970-113">Преобразует BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="a9970-113">Transforms the BoundingBox.</span></span><br/>                                                                 |
| [<span data-ttu-id="a9970-114">**контаинедби**</span><span class="sxs-lookup"><span data-stu-id="a9970-114">**ContainedBy**</span></span>](/windows/desktop/api/DirectXCollision/nf-directxcollision-boundingbox-containedby)<br/>           | <span data-ttu-id="a9970-115">Проверяет, содержится ли [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) в указанном фрустум.</span><span class="sxs-lookup"><span data-stu-id="a9970-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) is contained by the specified frustum.</span></span><br/> |
| [<span data-ttu-id="a9970-116">**креатефромсфере**</span><span class="sxs-lookup"><span data-stu-id="a9970-116">**CreateFromSphere**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfromsphere)<br/> | <span data-ttu-id="a9970-117">Создает BoundingBox, достаточно большой для размещения указанного Баундингсфере.</span><span class="sxs-lookup"><span data-stu-id="a9970-117">Creates a BoundingBox large enough to contain the a specified BoundingSphere.</span></span><br/>               |
| [<span data-ttu-id="a9970-118">**креатемержед**</span><span class="sxs-lookup"><span data-stu-id="a9970-118">**CreateMerged**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createmerged)<br/>         | <span data-ttu-id="a9970-119">Создает BoundingBox, достаточно большой для того, чтобы он содержал два заданных Баундбокс принимаемые экземпляры.</span><span class="sxs-lookup"><span data-stu-id="a9970-119">Creates a BoundingBox large enough to contains two specified BoundBox intances.</span></span><br/>             |
| [<span data-ttu-id="a9970-120">**Уголки**</span><span class="sxs-lookup"><span data-stu-id="a9970-120">**GetCorners**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-getcorners)<br/>             | <span data-ttu-id="a9970-121">Извлекает углы BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="a9970-121">Retrieves the corners of the BoundingBox.</span></span><br/>                                                   |
| [<span data-ttu-id="a9970-122">**\_назначение Op**</span><span class="sxs-lookup"><span data-stu-id="a9970-122">**op\_Assignment**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-operator-assign)<br/>      | <span data-ttu-id="a9970-123">Копирует значения из другого BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="a9970-123">Copies values from another BoundingBox.</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a9970-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a9970-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9970-125">BoundingBox</span><span class="sxs-lookup"><span data-stu-id="a9970-125">BoundingBox</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
