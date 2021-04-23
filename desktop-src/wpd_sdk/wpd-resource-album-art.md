---
description: Задает изображение, представляющее иллюстрацию альбома для объекта.
ms.assetid: 7a31ebb6-c4ab-4899-9c2e-c960aac4f0f9
title: WPD_RESOURCE_ALBUM_ART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4b800aa2ae22f2400f3195b85da6bd3bd35b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541231"
---
# <a name="wpd_resource_album_art"></a><span data-ttu-id="7c9b1-103">\_ \_ Обложка ресурсов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-103">WPD\_RESOURCE\_ALBUM\_ART</span></span>

<span data-ttu-id="7c9b1-104">Задает изображение, представляющее иллюстрацию альбома для объекта.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-104">Specifies an image that represents the album artwork for the object.</span></span>

<span data-ttu-id="7c9b1-105">Этот тип ресурса должен поддерживать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="7c9b1-106">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="7c9b1-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="7c9b1-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="7c9b1-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7c9b1-108">\_Ширина носителя \_ WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="7c9b1-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-109">Required.</span></span>                                              |
| [<span data-ttu-id="7c9b1-110">\_Высота устройства \_ WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="7c9b1-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-111">Required.</span></span>                                              |
| [<span data-ttu-id="7c9b1-112">\_ \_ \_ Общий \_ Размер атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="7c9b1-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-113">Required.</span></span>                                              |
| [<span data-ttu-id="7c9b1-114">\_атрибут ресурса \_ WPD \_ может \_ читать</span><span class="sxs-lookup"><span data-stu-id="7c9b1-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="7c9b1-115">Требуется, если клиенты могут читать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="7c9b1-116">\_атрибут ресурса \_ WPD \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="7c9b1-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="7c9b1-117">Требуется, если клиенты могут записывать в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="7c9b1-118">\_атрибут ресурса \_ WPD \_ может быть \_ удален</span><span class="sxs-lookup"><span data-stu-id="7c9b1-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="7c9b1-119">Требуется, если клиенты могут удалить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="7c9b1-120">\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="7c9b1-121">Требуется, если клиенты имеют доступ на чтение ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="7c9b1-122">\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_</span><span class="sxs-lookup"><span data-stu-id="7c9b1-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="7c9b1-123">Требуется, если клиенты имеют доступ на запись к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="7c9b1-124">\_ \_ Формат атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="7c9b1-125">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7c9b1-125">Required.</span></span>                                              |
| [<span data-ttu-id="7c9b1-126">\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="7c9b1-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="7c9b1-127">Рекомендуется</span><span class="sxs-lookup"><span data-stu-id="7c9b1-127">Recommended</span></span>                                            |



 

## <a name="see-also"></a><span data-ttu-id="7c9b1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c9b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9b1-129">**Требования к ресурсам**</span><span class="sxs-lookup"><span data-stu-id="7c9b1-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



