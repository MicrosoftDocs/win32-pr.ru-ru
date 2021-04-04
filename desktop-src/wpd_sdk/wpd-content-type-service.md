---
description: '\_ \_ Служба типа содержимого \_ WPD'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999163"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="02e8b-103">\_ \_ Служба типа содержимого \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="02e8b-104">Объект, описывающий его тип как \_ Служба типа содержимого WPD, \_ \_ представляет службу устройства.</span><span class="sxs-lookup"><span data-stu-id="02e8b-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="02e8b-105">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02e8b-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="02e8b-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="02e8b-106">Property Name</span></span>                                                                                        | <span data-ttu-id="02e8b-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="02e8b-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="02e8b-108">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="02e8b-109">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="02e8b-109">Required, read-only.</span></span> <span data-ttu-id="02e8b-110">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="02e8b-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="02e8b-111">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="02e8b-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="02e8b-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="02e8b-113">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="02e8b-114">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="02e8b-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="02e8b-115">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="02e8b-116">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="02e8b-116">Required, read-only.</span></span> <span data-ttu-id="02e8b-117">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="02e8b-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="02e8b-118">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="02e8b-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="02e8b-119">Требуется, если служба не должна отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="02e8b-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="02e8b-120">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="02e8b-121">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="02e8b-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="02e8b-122">\_Категория функционального \_ объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="02e8b-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="02e8b-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="02e8b-123">Required.</span></span> <span data-ttu-id="02e8b-124">Представляет тип службы устройства.</span><span class="sxs-lookup"><span data-stu-id="02e8b-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="02e8b-125">\_версия службы \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="02e8b-126">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="02e8b-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="02e8b-127">\_тип хранилища \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="02e8b-128">Требуется, если служба используется для хранения объектов.</span><span class="sxs-lookup"><span data-stu-id="02e8b-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="02e8b-129">\_емкость хранилища \_ WPD</span><span class="sxs-lookup"><span data-stu-id="02e8b-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="02e8b-130">Требуется, если служба используется для хранения объектов.</span><span class="sxs-lookup"><span data-stu-id="02e8b-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="02e8b-131">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02e8b-131">Typical Resources</span></span>

<span data-ttu-id="02e8b-132">Эти объекты не размещают ресурсы.</span><span class="sxs-lookup"><span data-stu-id="02e8b-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02e8b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="02e8b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e8b-134">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="02e8b-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



