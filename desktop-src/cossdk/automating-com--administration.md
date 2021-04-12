---
description: COM+ предоставляет объектную модель администрирования, которая предоставляет все функциональные возможности средства администрирования служб компонентов, а именно графический интерфейс, написанный на основе административных объектов.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Автоматизация администрирования COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142022"
---
# <a name="automating-com-administration"></a><span data-ttu-id="5fefc-103">Автоматизация администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="5fefc-103">Automating COM+ Administration</span></span>

<span data-ttu-id="5fefc-104">COM+ предоставляет объектную модель администрирования, которая предоставляет все функциональные возможности средства администрирования служб компонентов, а именно графический интерфейс, написанный на основе административных объектов.</span><span class="sxs-lookup"><span data-stu-id="5fefc-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="5fefc-105">Вы можете использовать эти объекты, предоставляемые библиотекой администрирования служб компонентов (Комадмин), для автоматизации всех задач администрирования приложений и служб COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="5fefc-106">Объекты Комадмин позволяют считывать и записывать данные, хранящиеся в каталоге COM+, базовое хранилище данных, которое содержит все данные конфигурации COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="5fefc-107">Эти объекты можно использовать для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="5fefc-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="5fefc-108">Создание и настройка приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="5fefc-109">Установка и экспорт существующих приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="5fefc-110">Управление установленными приложениями COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="5fefc-111">Управление службами и их настройка.</span><span class="sxs-lookup"><span data-stu-id="5fefc-111">Manage and configure services.</span></span>
-   <span data-ttu-id="5fefc-112">Удаленное администрирование служб компонентов на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="5fefc-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="5fefc-113">Можно использовать Комадмин объекты с поддержкой автоматизации, такие как Microsoft Visual Basic и Visual Basic Script.</span><span class="sxs-lookup"><span data-stu-id="5fefc-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="5fefc-114">Вы можете разрабатывать упрощенные сценарии или средства администрирования общего назначения.</span><span class="sxs-lookup"><span data-stu-id="5fefc-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="5fefc-115">Например, можно выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fefc-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="5fefc-116">Написание скриптов для выполнения задач администрирования.</span><span class="sxs-lookup"><span data-stu-id="5fefc-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="5fefc-117">Написание скриптов для автоматизации процессов разработки приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="5fefc-118">Разработка средств общего назначения для администрирования и мониторинга служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="5fefc-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="5fefc-119">Разработка исполняемых файлов программы установки для установки и развертывания приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="5fefc-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="5fefc-120">Библиотека Комадмин обеспечивает обратную совместимость с административной библиотекой MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="5fefc-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="5fefc-121">Большая часть существующего кода администрирования MTS 2,0 по-прежнему будет работать, хотя и с некоторыми исключениями.</span><span class="sxs-lookup"><span data-stu-id="5fefc-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="5fefc-122">(См. раздел [Библиотека администрирования MTS](mts-administration-library.md).)</span><span class="sxs-lookup"><span data-stu-id="5fefc-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="5fefc-123">Для эффективной автоматизации администрирования необходимо ознакомиться с задачами администрирования, выполняемыми с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="5fefc-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="5fefc-124">Полные описания объектов Комадмин и соответствующих интерфейсов см. в справочной документации по COM+ для следующих классов и интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="5fefc-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="5fefc-125">**комадминкаталог**</span><span class="sxs-lookup"><span data-stu-id="5fefc-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="5fefc-126">**комадминкаталогколлектион**</span><span class="sxs-lookup"><span data-stu-id="5fefc-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="5fefc-127">**комадминкаталогобжект**</span><span class="sxs-lookup"><span data-stu-id="5fefc-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="5fefc-128">**икомадминкаталог**</span><span class="sxs-lookup"><span data-stu-id="5fefc-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="5fefc-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="5fefc-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="5fefc-130">**икаталогколлектион**</span><span class="sxs-lookup"><span data-stu-id="5fefc-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="5fefc-131">**икаталогобжект**</span><span class="sxs-lookup"><span data-stu-id="5fefc-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="5fefc-132">В следующих подразделах этого раздела приводится обзор автоматизации администрирования с помощью объектов Комадмин:</span><span class="sxs-lookup"><span data-stu-id="5fefc-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="5fefc-133">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="5fefc-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="5fefc-134">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="5fefc-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="5fefc-135">Установка свойств и сохранение изменений в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="5fefc-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="5fefc-136">Обработка ошибок администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="5fefc-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="5fefc-137">Операции администрирования COM+ в транзакциях</span><span class="sxs-lookup"><span data-stu-id="5fefc-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="5fefc-138">Вводный пример с использованием каталога администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="5fefc-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 



