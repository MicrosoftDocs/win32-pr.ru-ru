---
description: Задачи секций COM+
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Задачи секций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262570"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="254e1-103">Задачи секций COM+</span><span class="sxs-lookup"><span data-stu-id="254e1-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="254e1-104">В следующих подразделах этого раздела приводятся пошаговые инструкции по использованию разделов COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="254e1-105">**Windows XP:** Возможность создания, настройки или делегирования разделов COM+ недоступна.</span><span class="sxs-lookup"><span data-stu-id="254e1-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="254e1-106">Глобальный раздел является единственным доступным разделом COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="254e1-107">\* \* Windows 2000: \* \* служба разделов COM+ недоступна в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="254e1-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="254e1-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="254e1-108">Topic</span></span>                                                                                                         | <span data-ttu-id="254e1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="254e1-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="254e1-110">Создание и Настройка разделов COM+</span><span class="sxs-lookup"><span data-stu-id="254e1-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="254e1-111">Описывает создание и настройку раздела COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="254e1-112">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="254e1-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="254e1-113">Описывает управление разделами COM+, которые не находятся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="254e1-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="254e1-114">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="254e1-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="254e1-115">Описывает, как управлять разделами COM+, указанными в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="254e1-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="254e1-116">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="254e1-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="254e1-117">Описание настройки прав доступа для раздела COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="254e1-118">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="254e1-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="254e1-119">Описание настройки приложений COM+ для принадлежности к разделу COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="254e1-120">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="254e1-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="254e1-121">Описывает, как выполнять получение данных о разделах COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="254e1-122">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="254e1-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="254e1-123">Описание настройки кэша разделов COM+.</span><span class="sxs-lookup"><span data-stu-id="254e1-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="254e1-124">Служба "разделы COM+" не включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="254e1-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="254e1-125">Чтобы использовать службу "разделы COM+", необходимо включить ее с помощью средства администрирования служб компонентов или путем изменения свойства Партитионсенаблед в коллекции [**локалкомпутер**](localcomputer.md) на true.</span><span class="sxs-lookup"><span data-stu-id="254e1-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="254e1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="254e1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="254e1-127">Основные понятия о разделах COM+</span><span class="sxs-lookup"><span data-stu-id="254e1-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




