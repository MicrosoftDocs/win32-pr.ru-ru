---
description: Что реплицируется
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Что реплицируется
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701221"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="e7611-103">Что реплицируется</span><span class="sxs-lookup"><span data-stu-id="e7611-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="e7611-104">Приложения</span><span class="sxs-lookup"><span data-stu-id="e7611-104">Applications</span></span>

<span data-ttu-id="e7611-105">Все приложения, установленные на исходном компьютере, реплицируются, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="e7611-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="e7611-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Не-COM + элементы и зависимости приложений</span><span class="sxs-lookup"><span data-stu-id="e7611-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="e7611-107">Администратор несет ответственность за репликацию любого объекта, от которого зависит приложение COM+, но которое неправильно входит в само приложение, например файлы данных и библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="e7611-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="e7611-108">COMREPL не будет реплицировать что-либо за пределы элементов приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="e7611-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="e7611-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Предварительно установленные приложения COM+</span><span class="sxs-lookup"><span data-stu-id="e7611-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="e7611-110">Приложения, которые используются внутри COM+ и устанавливаются с помощью программы установки COM+, не реплицируются.</span><span class="sxs-lookup"><span data-stu-id="e7611-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="e7611-111">следующие основные параметры.</span><span class="sxs-lookup"><span data-stu-id="e7611-111">These include the following:</span></span>

-   <span data-ttu-id="e7611-112">Системное приложение</span><span class="sxs-lookup"><span data-stu-id="e7611-112">System application</span></span>
-   <span data-ttu-id="e7611-113">Программы COM+</span><span class="sxs-lookup"><span data-stu-id="e7611-113">COM+ utilities</span></span>
-   <span data-ttu-id="e7611-114">Прослушиватель очереди недоставленных сообщений COM+ QC</span><span class="sxs-lookup"><span data-stu-id="e7611-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="e7611-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Приложения, созданные службами IIS</span><span class="sxs-lookup"><span data-stu-id="e7611-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="e7611-116">Эти приложения не реплицируются и включают следующее:</span><span class="sxs-lookup"><span data-stu-id="e7611-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="e7611-117">Внутрипроцессный приложения IIS</span><span class="sxs-lookup"><span data-stu-id="e7611-117">IIS in-process applications</span></span>
-   <span data-ttu-id="e7611-118">Служебные программы IIS</span><span class="sxs-lookup"><span data-stu-id="e7611-118">IIS utilities</span></span>
-   <span data-ttu-id="e7611-119">Все приложения, созданные для изолированных или виртуальных корней в составе пула</span><span class="sxs-lookup"><span data-stu-id="e7611-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="e7611-120">Список компьютеров</span><span class="sxs-lookup"><span data-stu-id="e7611-120">Computer List</span></span>

<span data-ttu-id="e7611-121">Удаленные компьютеры, имена которых находятся в папке **Computers** средства администрирования служб компонентов, не реплицируются с исходного компьютера на целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="e7611-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="e7611-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7611-122">Properties</span></span>

<span data-ttu-id="e7611-123">Реплицируются следующие свойства коллекции **локалкомпутер** :</span><span class="sxs-lookup"><span data-stu-id="e7611-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="e7611-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="e7611-124">TransactionTimeout</span></span>
-   <span data-ttu-id="e7611-125">ресаурцепулинженаблед</span><span class="sxs-lookup"><span data-stu-id="e7611-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="e7611-126">дкоменаблед</span><span class="sxs-lookup"><span data-stu-id="e7611-126">DCOMEnabled</span></span>
-   <span data-ttu-id="e7611-127">дефаултаусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="e7611-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="e7611-128">дефаултимперсонатионлевел</span><span class="sxs-lookup"><span data-stu-id="e7611-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="e7611-129">секурититраккинженаблед</span><span class="sxs-lookup"><span data-stu-id="e7611-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="e7611-130">Цисенаблед</span><span class="sxs-lookup"><span data-stu-id="e7611-130">CISEnabled</span></span>
-   <span data-ttu-id="e7611-131">секуререференцесенаблед</span><span class="sxs-lookup"><span data-stu-id="e7611-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="e7611-132">интернетпортслистед</span><span class="sxs-lookup"><span data-stu-id="e7611-132">InternetPortsListed</span></span>
-   <span data-ttu-id="e7611-133">деафулттоинтернетпортс</span><span class="sxs-lookup"><span data-stu-id="e7611-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="e7611-134">Порты</span><span class="sxs-lookup"><span data-stu-id="e7611-134">Ports</span></span>
-   <span data-ttu-id="e7611-135">рпкпроксенаблед</span><span class="sxs-lookup"><span data-stu-id="e7611-135">RpcProxyEnabled</span></span>

<span data-ttu-id="e7611-136">Следующие свойства коллекции **локалкомпутер** не реплицируются:</span><span class="sxs-lookup"><span data-stu-id="e7611-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="e7611-137">Описание</span><span class="sxs-lookup"><span data-stu-id="e7611-137">Description</span></span>
-   <span data-ttu-id="e7611-138">аппликатионпроксирсн</span><span class="sxs-lookup"><span data-stu-id="e7611-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="e7611-139">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="e7611-139">IsRouter</span></span>

<span data-ttu-id="e7611-140">Описание свойств коллекции **локалкомпутер** см. в разделе [**локалкомпутер**](localcomputer.md).</span><span class="sxs-lookup"><span data-stu-id="e7611-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7611-141">См. также</span><span class="sxs-lookup"><span data-stu-id="e7611-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7611-142">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="e7611-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="e7611-143">Ведение журнала и отчеты об ошибках</span><span class="sxs-lookup"><span data-stu-id="e7611-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="e7611-144">Этапы репликации</span><span class="sxs-lookup"><span data-stu-id="e7611-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="e7611-145">Использование COMREPL</span><span class="sxs-lookup"><span data-stu-id="e7611-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 



