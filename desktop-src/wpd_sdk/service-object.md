---
description: Объект службы
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Объект службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913288"
---
# <a name="service-object"></a><span data-ttu-id="b8fa3-103">Объект службы</span><span class="sxs-lookup"><span data-stu-id="b8fa3-103">Service Object</span></span>

<span data-ttu-id="b8fa3-104">Объект службы должен поддерживать следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="b8fa3-105">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="b8fa3-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="b8fa3-106">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="b8fa3-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8fa3-107">[\_идентификатор объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="b8fa3-108">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-108">Required.</span></span> <span data-ttu-id="b8fa3-109">.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-109">.</span></span>                                                                           |
| <span data-ttu-id="b8fa3-110">[\_ \_ идентификатор родительского объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="b8fa3-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-111">Required.</span></span>                                                                             |
| <span data-ttu-id="b8fa3-112">[\_имя объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="b8fa3-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-113">Required.</span></span>                                                                             |
| <span data-ttu-id="b8fa3-114">[\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="b8fa3-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-115">Required.</span></span>                                                                             |
| <span data-ttu-id="b8fa3-116">[\_объект WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="b8fa3-117">Требуется, если объект службы не должен отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="b8fa3-118">[\_система объектов \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="b8fa3-119">Требуется, если объект является системным объектом (например, он представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="b8fa3-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="b8fa3-120">[\_Категория функционального \_ объекта WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="b8fa3-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-121">Required.</span></span> <span data-ttu-id="b8fa3-122">Представляет тип службы устройства, например Контакты службы.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="b8fa3-123">[\_версия службы \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="b8fa3-124">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-124">Required.</span></span>                                                                             |
| <span data-ttu-id="b8fa3-125">[\_тип хранилища \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="b8fa3-126">Требуется, если служба используется для хранения объектов.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="b8fa3-127">[\_емкость хранилища \_ WPD](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8fa3-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="b8fa3-128">Требуется, если служба используется для хранения объектов.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="b8fa3-129">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b8fa3-129">Typical Resources</span></span>

<span data-ttu-id="b8fa3-130">Обычно эти объекты не размещают ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="b8fa3-131">Стандартные форматы</span><span class="sxs-lookup"><span data-stu-id="b8fa3-131">Typical Formats</span></span>

<span data-ttu-id="b8fa3-132">В следующем списке приведены типичные форматы, используемые объектом службы.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="b8fa3-133">Однако этот объект не ограничен этими форматами.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="b8fa3-134">\_Формат объекта WPD не \_ \_ указан</span><span class="sxs-lookup"><span data-stu-id="b8fa3-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8fa3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b8fa3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8fa3-136">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="b8fa3-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 
