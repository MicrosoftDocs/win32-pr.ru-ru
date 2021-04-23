---
description: Записи — это способ обмена данными между узлами в графе или членами группы.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999022"
---
# <a name="records"></a><span data-ttu-id="04ffa-103">Записи</span><span class="sxs-lookup"><span data-stu-id="04ffa-103">Records</span></span>

<span data-ttu-id="04ffa-104">Записи — это способ обмена данными между узлами в графе или членами группы.</span><span class="sxs-lookup"><span data-stu-id="04ffa-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="04ffa-105">Запись состоит из следующих двух частей:</span><span class="sxs-lookup"><span data-stu-id="04ffa-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="04ffa-106">Заголовок записи</span><span class="sxs-lookup"><span data-stu-id="04ffa-106">Record header</span></span>
-   <span data-ttu-id="04ffa-107">Определенное Непрозрачное содержимое данных</span><span class="sxs-lookup"><span data-stu-id="04ffa-107">Specific opaque data content</span></span>

<span data-ttu-id="04ffa-108">Заголовок содержит сведения о записи, включая версию, создателя и тип публикуемых данных.</span><span class="sxs-lookup"><span data-stu-id="04ffa-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="04ffa-109">Заголовок также содержит поле атрибутов XML, которое позволяет приложениям добавлять атрибуты name-value, описывающие данные, а также эффективный поиск в базе данных записей для конкретных записей, которые ранее были опубликованы.</span><span class="sxs-lookup"><span data-stu-id="04ffa-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="04ffa-110">Содержимое — это определяемые приложением данные, которые непрозрачны для одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="04ffa-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="04ffa-111">Когда запись публикуется, она (заголовок и данные) передается на весь граф или группу.</span><span class="sxs-lookup"><span data-stu-id="04ffa-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="04ffa-112">Синхронизированные одноранговые узлы получают эти данные и сохраняют их в локальной базе данных.</span><span class="sxs-lookup"><span data-stu-id="04ffa-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="04ffa-113">Несинхронизированные и автономные одноранговые узлы получают данные при следующем подключении и синхронизации с одноранговой диаграммой или группой.</span><span class="sxs-lookup"><span data-stu-id="04ffa-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="04ffa-114">Сведения о работе с записями см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="04ffa-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="04ffa-115">Зависимости записей</span><span class="sxs-lookup"><span data-stu-id="04ffa-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="04ffa-116">Управление записями</span><span class="sxs-lookup"><span data-stu-id="04ffa-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="04ffa-117">Схема атрибута записи</span><span class="sxs-lookup"><span data-stu-id="04ffa-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="04ffa-118">Формат запроса поиска записей</span><span class="sxs-lookup"><span data-stu-id="04ffa-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 



