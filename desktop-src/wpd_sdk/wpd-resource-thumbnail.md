---
description: Задает небольшое изображение&\# 8212; обычно это уменьшенная версия более крупного изображения в объекте.
ms.assetid: ad1eac9d-b182-49b2-bd2c-2d76e2026d80
title: WPD_RESOURCE_THUMBNAIL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc26af624f756f55ccb10ccf3f8c7bf3e6a6035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144695"
---
# <a name="wpd_resource_thumbnail"></a><span data-ttu-id="5af9a-103">\_эскиз ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-103">WPD\_RESOURCE\_THUMBNAIL</span></span>

<span data-ttu-id="5af9a-104">Задает небольшое изображение — обычно это уменьшенная версия более крупного изображения в объекте.</span><span class="sxs-lookup"><span data-stu-id="5af9a-104">Specifies a small picture—typically a smaller version of a larger picture in the object.</span></span>

<span data-ttu-id="5af9a-105">Этот тип ресурса должен поддерживать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="5af9a-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="5af9a-106">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="5af9a-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="5af9a-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="5af9a-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5af9a-108">\_Ширина носителя \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="5af9a-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5af9a-109">Required.</span></span>                                              |
| [<span data-ttu-id="5af9a-110">\_Высота устройства \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="5af9a-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5af9a-111">Required.</span></span>                                              |
| [<span data-ttu-id="5af9a-112">\_ \_ \_ Общий \_ Размер атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="5af9a-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5af9a-113">Required.</span></span>                                              |
| [<span data-ttu-id="5af9a-114">\_атрибут ресурса \_ WPD \_ может \_ читать</span><span class="sxs-lookup"><span data-stu-id="5af9a-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="5af9a-115">Требуется, если клиенты могут читать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5af9a-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="5af9a-116">\_атрибут ресурса \_ WPD \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="5af9a-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="5af9a-117">Требуется, если клиенты могут записывать в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5af9a-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="5af9a-118">\_атрибут ресурса \_ WPD \_ может быть \_ удален</span><span class="sxs-lookup"><span data-stu-id="5af9a-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="5af9a-119">Требуется, если клиенты могут удалить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5af9a-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="5af9a-120">\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="5af9a-121">Требуется, если клиенты имеют доступ на чтение ресурса.</span><span class="sxs-lookup"><span data-stu-id="5af9a-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="5af9a-122">\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_</span><span class="sxs-lookup"><span data-stu-id="5af9a-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="5af9a-123">Требуется, если клиенты имеют доступ на запись к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="5af9a-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="5af9a-124">\_ \_ Формат атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="5af9a-125">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5af9a-125">Required.</span></span>                                              |
| [<span data-ttu-id="5af9a-126">\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5af9a-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="5af9a-127">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="5af9a-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="5af9a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5af9a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af9a-129">**Требования к ресурсам**</span><span class="sxs-lookup"><span data-stu-id="5af9a-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



