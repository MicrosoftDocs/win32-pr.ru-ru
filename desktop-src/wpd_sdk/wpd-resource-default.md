---
description: Задает весь файл за объектом. Это также способ обращения к любому типу ресурсов, включая те, которые не охватываются другими типами ресурсов переносных устройств Windows, такими как тип настраиваемого объекта.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546546"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="45ffc-104">\_ресурс \_ по умолчанию для WPD</span><span class="sxs-lookup"><span data-stu-id="45ffc-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="45ffc-105">Задает весь файл за объектом.</span><span class="sxs-lookup"><span data-stu-id="45ffc-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="45ffc-106">Это также способ обращения к любому типу ресурсов, включая те, которые не охватываются другими типами ресурсов переносных устройств Windows, такими как тип настраиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="45ffc-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="45ffc-107">Будут включаться все ресурсы, внедренные в указанный ресурс.</span><span class="sxs-lookup"><span data-stu-id="45ffc-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="45ffc-108">Например, ресурсом по умолчанию корневой папки Contacts могут быть все вложенные контакты.</span><span class="sxs-lookup"><span data-stu-id="45ffc-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="45ffc-109">Однако все дочерние ресурсы, которые *связаны* только с метаданными или ссылками, не включаются.</span><span class="sxs-lookup"><span data-stu-id="45ffc-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="45ffc-110">В качестве примера можно привести список воспроизведения, который может ссылаться только на звуковые файлы через ссылки на метаданные или ссылки на текстовые пути в файле.</span><span class="sxs-lookup"><span data-stu-id="45ffc-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="45ffc-111">Единственным допустимым значением *PID* для этого **PROPERTYKEY** является нуль.</span><span class="sxs-lookup"><span data-stu-id="45ffc-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="45ffc-112">Этот тип ресурса должен поддерживать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="45ffc-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="45ffc-113">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="45ffc-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="45ffc-114">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="45ffc-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="45ffc-115">\_ \_ \_ Общий \_ Размер атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="45ffc-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="45ffc-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="45ffc-116">Required.</span></span>                                              |
| [<span data-ttu-id="45ffc-117">\_атрибут ресурса \_ WPD \_ может \_ читать</span><span class="sxs-lookup"><span data-stu-id="45ffc-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="45ffc-118">Требуется, если клиенты могут читать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="45ffc-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="45ffc-119">\_атрибут ресурса \_ WPD \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="45ffc-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="45ffc-120">Требуется, если клиенты могут записывать в этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="45ffc-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="45ffc-121">\_атрибут ресурса \_ WPD \_ может быть \_ удален</span><span class="sxs-lookup"><span data-stu-id="45ffc-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="45ffc-122">Требуется, если клиенты могут удалить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="45ffc-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="45ffc-123">\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD</span><span class="sxs-lookup"><span data-stu-id="45ffc-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="45ffc-124">Требуется, если клиенты имеют доступ на чтение ресурса.</span><span class="sxs-lookup"><span data-stu-id="45ffc-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="45ffc-125">\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_</span><span class="sxs-lookup"><span data-stu-id="45ffc-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="45ffc-126">Требуется, если клиенты имеют доступ на запись к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="45ffc-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="45ffc-127">\_ \_ Формат атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="45ffc-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="45ffc-128">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="45ffc-128">Required.</span></span>                                              |
| [<span data-ttu-id="45ffc-129">\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD</span><span class="sxs-lookup"><span data-stu-id="45ffc-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="45ffc-130">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="45ffc-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="45ffc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45ffc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ffc-132">**Требования к ресурсам**</span><span class="sxs-lookup"><span data-stu-id="45ffc-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



