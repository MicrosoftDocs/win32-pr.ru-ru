---
description: Указывает тип ресурса, не определенный другими портативными устройствами Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144698"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="755cd-103">\_универсальный ресурс \_ WPD</span><span class="sxs-lookup"><span data-stu-id="755cd-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="755cd-104">Указывает тип ресурса, не определенный другими портативными устройствами Windows.</span><span class="sxs-lookup"><span data-stu-id="755cd-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="755cd-105">Вы можете определить собственные настраиваемые ресурсы, которые поддерживают любые настраиваемые атрибуты или определенные портативные устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="755cd-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="755cd-106">Однако любой созданный ресурс должен поддерживать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="755cd-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="755cd-107">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="755cd-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="755cd-108">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="755cd-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="755cd-109">\_ \_ \_ Общий \_ Размер атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="755cd-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="755cd-110">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="755cd-110">Required.</span></span>                                              |
| [<span data-ttu-id="755cd-111">\_атрибут ресурса \_ WPD \_ может \_ читать</span><span class="sxs-lookup"><span data-stu-id="755cd-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="755cd-112">Требуется, если клиенты могут читать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="755cd-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="755cd-113">\_атрибут ресурса \_ WPD \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="755cd-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="755cd-114">Требуется, если клиенты могут записывать в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="755cd-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="755cd-115">\_атрибут ресурса \_ WPD \_ может быть \_ удален</span><span class="sxs-lookup"><span data-stu-id="755cd-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="755cd-116">Требуется, если клиенты могут удалить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="755cd-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="755cd-117">\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="755cd-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="755cd-118">Требуется, если клиенты имеют доступ на чтение ресурса.</span><span class="sxs-lookup"><span data-stu-id="755cd-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="755cd-119">\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_</span><span class="sxs-lookup"><span data-stu-id="755cd-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="755cd-120">Требуется, если клиенты имеют доступ на запись к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="755cd-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="755cd-121">\_ \_ Формат атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="755cd-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="755cd-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="755cd-122">Required.</span></span>                                              |
| [<span data-ttu-id="755cd-123">\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="755cd-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="755cd-124">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="755cd-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="755cd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="755cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755cd-126">**Требования к ресурсам**</span><span class="sxs-lookup"><span data-stu-id="755cd-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



