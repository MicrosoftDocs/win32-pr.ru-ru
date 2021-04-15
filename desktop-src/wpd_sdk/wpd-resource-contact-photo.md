---
description: Задает изображение, представляющее фотографию лица, на которое ссылается объект Contact.
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701431"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="5701b-103">\_фотография контакта по ресурсу WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="5701b-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="5701b-104">Задает изображение, представляющее фотографию лица, на которое ссылается объект Contact.</span><span class="sxs-lookup"><span data-stu-id="5701b-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="5701b-105">Этот тип ресурса должен поддерживать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="5701b-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="5701b-106">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="5701b-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="5701b-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="5701b-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5701b-108">\_Ширина носителя \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5701b-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="5701b-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5701b-109">Required.</span></span>                                              |
| [<span data-ttu-id="5701b-110">\_Высота устройства \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5701b-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="5701b-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5701b-111">Required.</span></span>                                              |
| [<span data-ttu-id="5701b-112">\_ \_ \_ Общий \_ Размер атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="5701b-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="5701b-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5701b-113">Required.</span></span>                                              |
| [<span data-ttu-id="5701b-114">\_атрибут ресурса \_ WPD \_ может \_ читать</span><span class="sxs-lookup"><span data-stu-id="5701b-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="5701b-115">Требуется, если клиенты могут читать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5701b-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="5701b-116">\_атрибут ресурса \_ WPD \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="5701b-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="5701b-117">Требуется, если клиенты могут записывать в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5701b-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="5701b-118">\_атрибут ресурса \_ WPD \_ может быть \_ удален</span><span class="sxs-lookup"><span data-stu-id="5701b-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="5701b-119">Требуется, если клиенты могут удалить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5701b-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="5701b-120">\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="5701b-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="5701b-121">Требуется, если клиенты имеют доступ на чтение ресурса.</span><span class="sxs-lookup"><span data-stu-id="5701b-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="5701b-122">\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_</span><span class="sxs-lookup"><span data-stu-id="5701b-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="5701b-123">Требуется, если клиенты имеют доступ на запись к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="5701b-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="5701b-124">\_ \_ Формат атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5701b-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="5701b-125">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5701b-125">Required.</span></span>                                              |
| [<span data-ttu-id="5701b-126">\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5701b-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="5701b-127">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="5701b-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="5701b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5701b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5701b-129">**Требования к ресурсам**</span><span class="sxs-lookup"><span data-stu-id="5701b-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



