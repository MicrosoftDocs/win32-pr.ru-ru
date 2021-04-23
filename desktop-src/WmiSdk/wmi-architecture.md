---
description: Инструментарий WMI предоставляет унифицированный интерфейс для всех локальных или удаленных приложений или сценариев, которые получают данные управления из компьютерной системы, сети или предприятия.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Архитектура WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555962"
---
# <a name="wmi-architecture"></a><span data-ttu-id="cd355-103">Архитектура WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-103">WMI Architecture</span></span>

<span data-ttu-id="cd355-104">Инструментарий WMI предоставляет унифицированный интерфейс для всех локальных или удаленных приложений или сценариев, которые получают данные управления из компьютерной системы, сети или предприятия.</span><span class="sxs-lookup"><span data-stu-id="cd355-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="cd355-105">Унифицированный интерфейс разработан таким образом, что клиентским приложениям и сценариям WMI не нужно вызывать широкий спектр программных интерфейсов (API) операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cd355-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="cd355-106">Многие API не могут вызываться клиентами автоматизации, такими как скрипты или приложения Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cd355-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="cd355-107">Другие API не выполняют вызовы к удаленным компьютерам.</span><span class="sxs-lookup"><span data-stu-id="cd355-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="cd355-108">Чтобы получить данные из WMI, напишите клиентский скрипт или приложение, обращающееся к [классам WMI](wmi-classes.md) , или предоставьте данные в WMI, записав [*поставщик WMI*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="cd355-109">Дополнительные сведения см. [в разделе Использование WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="cd355-110">Объекты, потребители и инфраструктура WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="cd355-111">На следующей схеме показана связь между инфраструктурой WMI и поставщиками WMI и управляемыми объектами, а также показывается связь между инфраструктурой WMI и потребителями WMI.</span><span class="sxs-lookup"><span data-stu-id="cd355-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![отношение между инфраструктурой WMI, поставщиками WMI и управляемыми объектами](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="cd355-113">Компоненты WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-113">WMI Components</span></span>

<span data-ttu-id="cd355-114">В следующем списке описываются ключевые компоненты WMI.</span><span class="sxs-lookup"><span data-stu-id="cd355-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="cd355-115">Управляемые объекты и поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="cd355-116">Поставщик WMI — это COM-объект, который наблюдает за одним или несколькими [*управляемыми объектами*](gloss-m.md) для WMI.</span><span class="sxs-lookup"><span data-stu-id="cd355-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="cd355-117">Управляемый объект — это логический или физический компонент предприятия, такой как жесткий диск, сетевой адаптер, система базы данных, операционная система, процесс или служба.</span><span class="sxs-lookup"><span data-stu-id="cd355-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="cd355-118">Подобно драйверу, поставщик предоставляет инструментарий WMI с данными из управляемого объекта и обрабатывает сообщения от WMI управляемому объекту.</span><span class="sxs-lookup"><span data-stu-id="cd355-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="cd355-119">Поставщики WMI состоят из DLL-файла и файла [*MOF-файл (MOF)*](gloss-m.md) , определяющего классы, для которых поставщик возвращает данные и выполняет операции.</span><span class="sxs-lookup"><span data-stu-id="cd355-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="cd355-120">Поставщики, например приложения WMI C++, используют [API COM для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="cd355-121">Дополнительные сведения см. [в разделе Предоставление данных инструментарию WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="cd355-122">Примером поставщика является предварительно установленный [поставщик реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), который обращается к данным в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="cd355-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="cd355-123">Поставщик реестра имеет один [*класс WMI*](gloss-w.md) [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov)с множеством методов, но не имеет свойств.</span><span class="sxs-lookup"><span data-stu-id="cd355-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="cd355-124">Другие предварительно установленные поставщики, такие как [поставщик Win32](/windows/desktop/CIMWin32Prov/win32-provider), обычно имеют классы со многими свойствами, но с несколькими методами, такими как [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) или [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="cd355-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="cd355-125">DLL-файл поставщика реестра, Stdprov.dll, содержит код, который динамически возвращает данные при запросе клиентскими скриптами или приложениями.</span><span class="sxs-lookup"><span data-stu-id="cd355-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="cd355-126">Файлы WMI MOF и DLL находятся в папке% WINDIR% \\ system32 \\ WBEM, а также в [инструментарии WMI Command-Line средства](wmi-command-line-tools.md), такие как [**Winmgmt.exe**](winmgmt.md) и [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="cd355-127">Классы поставщиков, такие как [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), ОПРЕДЕЛЯЮТся в MOF-файлах, а затем компилируются в репозиторий WMI при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="cd355-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="cd355-128">Инфраструктура WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="cd355-129">Инфраструктура WMI — это компонент операционной системы Microsoft Windows, известный как служба WMI (winmgmt).</span><span class="sxs-lookup"><span data-stu-id="cd355-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="cd355-130">В инфраструктуре WMI есть два компонента: ядро WMI и [*репозиторий WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="cd355-131">Репозиторий WMI упорядочен по [*пространствам имен*](gloss-n.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="cd355-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="cd355-132">Служба WMI создает некоторые пространства имен, такие как корневая папка \\ по умолчанию root \\ CIMV2 и корневая \\ Подписка при запуске системы, и предварительно устанавливает набор определений классов по умолчанию, включая [Классы Win32](/windows/desktop/CIMWin32Prov/win32-provider), [системные классы WMI](wmi-system-classes.md)и другие.</span><span class="sxs-lookup"><span data-stu-id="cd355-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="cd355-133">Остальные пространства имен, обнаруженные в системе, создаются поставщиками для других частей операционной системы или продуктов.</span><span class="sxs-lookup"><span data-stu-id="cd355-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="cd355-134">Дополнительные сведения и список поставщиков WMI, найденных в большинстве версий операционных систем, см. в разделе [поставщики WMI](wmi-providers.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="cd355-135">Служба WMI выступает в качестве посредника между поставщиками, приложениями управления и репозиторием WMI.</span><span class="sxs-lookup"><span data-stu-id="cd355-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="cd355-136">В репозитории хранятся только статические данные об объектах, например классы, определенные поставщиками.</span><span class="sxs-lookup"><span data-stu-id="cd355-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="cd355-137">Инструментарий WMI динамически получает данные от поставщика, когда клиент запрашивает его.</span><span class="sxs-lookup"><span data-stu-id="cd355-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="cd355-138">Кроме того, можно настроить подписки на получение уведомлений о событиях от поставщика.</span><span class="sxs-lookup"><span data-stu-id="cd355-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="cd355-139">Дополнительные сведения см. в разделе [наблюдение за событиями](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="cd355-140">Потребители WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-140">WMI consumers</span></span>

    <span data-ttu-id="cd355-141">Потребитель WMI — это приложение управления или сценарий, взаимодействующий с инфраструктурой WMI.</span><span class="sxs-lookup"><span data-stu-id="cd355-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="cd355-142">Приложение управления может запрашивать, перечислять данные, выполнять методы поставщиков или подписываться на события, вызывая [API COM для инструментария WMI](com-api-for-wmi.md) или [API скриптов для WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cd355-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="cd355-143">Единственными данными или действиями, доступными для управляемого объекта, например дискового накопителя или службы, являются те, которые предоставляет поставщик.</span><span class="sxs-lookup"><span data-stu-id="cd355-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd355-144">См. также</span><span class="sxs-lookup"><span data-stu-id="cd355-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd355-145">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="cd355-146">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="cd355-147">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="cd355-148">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="cd355-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="cd355-149">Предоставление данных инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="cd355-150">Классы WMI</span><span class="sxs-lookup"><span data-stu-id="cd355-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="cd355-151">Мониторинг событий</span><span class="sxs-lookup"><span data-stu-id="cd355-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="cd355-152">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="cd355-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
