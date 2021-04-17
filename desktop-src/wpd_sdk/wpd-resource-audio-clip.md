---
description: Указывает аудиоклип для объекта.
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674195"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="6b8fc-103">\_ \_ звуковой ролик ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="6b8fc-104">Указывает аудиоклип для объекта.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="6b8fc-105">Этот тип ресурса должен поддерживать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="6b8fc-106">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="6b8fc-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="6b8fc-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="6b8fc-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="6b8fc-108">\_звуковая \_ скорость WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="6b8fc-109">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="6b8fc-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="6b8fc-110">\_число звуковых \_ каналов WPD \_</span><span class="sxs-lookup"><span data-stu-id="6b8fc-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="6b8fc-111">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-111">Optional.</span></span>                                              |
| [<span data-ttu-id="6b8fc-112">\_код звукового \_ формата WPD \_</span><span class="sxs-lookup"><span data-stu-id="6b8fc-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="6b8fc-113">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-113">Optional.</span></span>                                              |
| [<span data-ttu-id="6b8fc-114">\_ \_ Битовая глубина звука \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="6b8fc-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-115">Optional.</span></span>                                              |
| [<span data-ttu-id="6b8fc-116">\_Выравнивание аудио \_ блока \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="6b8fc-117">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-117">Optional.</span></span>                                              |
| [<span data-ttu-id="6b8fc-118">\_ \_ \_ Общий \_ Размер атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="6b8fc-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-119">Required.</span></span>                                              |
| [<span data-ttu-id="6b8fc-120">\_атрибут ресурса \_ WPD \_ может \_ читать</span><span class="sxs-lookup"><span data-stu-id="6b8fc-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="6b8fc-121">Требуется, если клиенты могут читать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="6b8fc-122">\_атрибут ресурса \_ WPD \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="6b8fc-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="6b8fc-123">Требуется, если клиенты могут записывать в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="6b8fc-124">\_атрибут ресурса \_ WPD \_ может быть \_ удален</span><span class="sxs-lookup"><span data-stu-id="6b8fc-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="6b8fc-125">Требуется, если клиенты могут удалить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="6b8fc-126">\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="6b8fc-127">Требуется, если клиенты имеют доступ на чтение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="6b8fc-128">\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_</span><span class="sxs-lookup"><span data-stu-id="6b8fc-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="6b8fc-129">Требуется, если клиенты имеют доступ на запись к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="6b8fc-130">\_ \_ Формат атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="6b8fc-131">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6b8fc-131">Required.</span></span>                                              |
| [<span data-ttu-id="6b8fc-132">\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6b8fc-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="6b8fc-133">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="6b8fc-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="6b8fc-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b8fc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8fc-135">**Требования к ресурсам**</span><span class="sxs-lookup"><span data-stu-id="6b8fc-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



