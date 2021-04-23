---
description: Установщик Windows является рекомендуемым решением для установки и настройки приложений в Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Руководство на основе ролей для установщик Windows документации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080472"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="bcd5b-103">Руководство на основе ролей для установщик Windows документации</span><span class="sxs-lookup"><span data-stu-id="bcd5b-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="bcd5b-104">Установщик Windows является рекомендуемым решением для установки и настройки приложений в Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="bcd5b-105">Поэтому некоторые сведения, содержащиеся в этом пакете SDK, будут интересны для широкого спектра разработки программного обеспечения и ИТ-специалистов.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="bcd5b-106">Этот раздел представлен в качестве руководства для читателей, которые предпочитают просматривать ссылки на разделы, упорядоченные по сценариям Professional Role и Common Task.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="bcd5b-107">Поскольку роли могут сильно различаться в разных организациях, приведенная ниже группировка должна рассматриваться в качестве пути к расположению, чтобы начать поиск необходимой информации.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="bcd5b-108">Разработчики приложений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="bcd5b-109">Авторы программы установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="bcd5b-110">ИТ-специалисты</span><span class="sxs-lookup"><span data-stu-id="bcd5b-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="bcd5b-111">Разработчики инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="bcd5b-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="bcd5b-112">Эта документация предназначена для разработчиков программного обеспечения, которые хотят создавать приложения, использующие установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="bcd5b-113">В качестве основного источника справочных материалов по установщику пакет SDK предоставляет сведения о пакетах установки и службе установщика.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="bcd5b-114">Он содержит полные описания прикладного программного интерфейса (API) и элементов базы данных установщика.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="bcd5b-115">Дополнительные сведения см. в разделе [другие источники сведений о установщик Windows](other-sources-of-windows-installer-information.md).</span><span class="sxs-lookup"><span data-stu-id="bcd5b-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="bcd5b-116">Разработчики приложений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-116">Application Developers</span></span>

<span data-ttu-id="bcd5b-117">Разработчики приложений создают приложения, вызывающие установщик Windows программный интерфейс приложения и устанавливающие пакеты установщика Windows во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="bcd5b-118">Установщик Windows может выполнять работу в таких приложениях, как самостоятельное восстановление и установка по запросу.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="bcd5b-119">Как правило, разработчики приложений выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="bcd5b-120">Включить установку по запросу приложений во время выполнения из другого приложения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="bcd5b-121">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-122">Использование функций установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="bcd5b-123">Справочник по функциям установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-124">Установка по запросу</span><span class="sxs-lookup"><span data-stu-id="bcd5b-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="bcd5b-125">Управление компонентами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="bcd5b-126">Изменение ярлыков установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="bcd5b-127">**Олеадвтсуппорт, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="bcd5b-128">Поддержка платформ объявления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="bcd5b-129">Включение самостоятельного восстановления приложений путем повторной установки компонентов при необходимости во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="bcd5b-130">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-131">Использование функций установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="bcd5b-132">Справочник по функциям установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-133">Устойчивость</span><span class="sxs-lookup"><span data-stu-id="bcd5b-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="bcd5b-134">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="bcd5b-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="bcd5b-135">Поиск неработающей функции или компонента</span><span class="sxs-lookup"><span data-stu-id="bcd5b-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="bcd5b-136">Замена существующих файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="bcd5b-137">Отображать пользовательский интерфейс для получения сведений о пользователях и предпочтениях конфигурации при первом установке или запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="bcd5b-138">Пользовательский интерфейс должен быть добавлен автором установки пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="bcd5b-139">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-140">Использование функций установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="bcd5b-141">Инициализация приложения</span><span class="sxs-lookup"><span data-stu-id="bcd5b-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="bcd5b-142">Диалоговое окно файла firstrun</span><span class="sxs-lookup"><span data-stu-id="bcd5b-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="bcd5b-143">Сведения о пользовательском интерфейсе</span><span class="sxs-lookup"><span data-stu-id="bcd5b-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="bcd5b-144">Создание приложений, использующих косвенную модель, для ссылки на компоненты с параллельными функциями.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="bcd5b-145">Полные категории компонентов должны добавляться автором установки пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="bcd5b-146">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-147">Компоненты с квалификаторами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="bcd5b-148">Использование полных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="bcd5b-149">Используйте закрытые и параллельные сборки для изоляции приложений и уменьшения конфликтов DLL.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="bcd5b-150">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-151">Сборки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="bcd5b-152">Разделы реестра сборки, записанные установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="bcd5b-153">Установка сборок Win32 для параллельного совместного использования в Windows XP</span><span class="sxs-lookup"><span data-stu-id="bcd5b-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="bcd5b-154">Установка сборок Win32 для закрытого использования приложения в Windows XP</span><span class="sxs-lookup"><span data-stu-id="bcd5b-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="bcd5b-155">Таблица Мсиассембли</span><span class="sxs-lookup"><span data-stu-id="bcd5b-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="bcd5b-156">Таблица Мсиассемблинаме</span><span class="sxs-lookup"><span data-stu-id="bcd5b-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="bcd5b-157">**мсипровидеассембли**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="bcd5b-158">**MsiWin32AssemblySupport, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="bcd5b-159">**Мсинетассемблисуппорт, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="bcd5b-160">**Изолированные компоненты**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="bcd5b-161">Подготовьте приложение для установки собственных основных обновлений.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="bcd5b-162">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-163">Установка исправлений и обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="bcd5b-164">Основные обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="bcd5b-165">**UpgradeCode, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="bcd5b-166">**Использование UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="bcd5b-167">Предотвращение установки старого пакета более новой версией</span><span class="sxs-lookup"><span data-stu-id="bcd5b-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="bcd5b-168">Подготовьте приложение, чтобы установить собственные незначительные обновления, небольшие обновления или исправления.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="bcd5b-169">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-170">Установка исправлений и обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="bcd5b-171">Небольшие обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="bcd5b-172">Незначительные обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="bcd5b-173">Упорядочите ресурсы приложения в компоненты, которые могут работать с установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="bcd5b-174">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-175">Компоненты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="bcd5b-176">Работа с функциями и компонентами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="bcd5b-177">Использование транзитивных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="bcd5b-178">Что произойдет, если правила компонентов будут разорваны?</span><span class="sxs-lookup"><span data-stu-id="bcd5b-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="bcd5b-179">Упорядочение приложений по компонентам</span><span class="sxs-lookup"><span data-stu-id="bcd5b-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="bcd5b-180">Изолированные компоненты</span><span class="sxs-lookup"><span data-stu-id="bcd5b-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="bcd5b-181">Компоненты с квалификаторами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="bcd5b-182">Авторы программы установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-182">Setup Authors</span></span>

<span data-ttu-id="bcd5b-183">Авторы программы установки создают установщик Windows пакеты (MSI-файлы), которые содержат логику установки и сведения, необходимые для установки приложения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="bcd5b-184">Обычно они используют средства разработки, такие как [Orca.exe](orca-exe.md) для заполнения базы данных установщик Windows с помощью логики и информации программы установки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="bcd5b-185">Как правило, авторы программы установки выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="bcd5b-186">Определите функциональные возможности, доступные в разных версиях установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="bcd5b-187">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-188">Определение версии установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="bcd5b-189">Выпущенные версии установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="bcd5b-190">Новые возможности установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="bcd5b-191">Упорядочивайте ресурсы приложений в установщик Windows компоненты.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="bcd5b-192">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-193">Компоненты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="bcd5b-194">Упорядочение приложений по компонентам</span><span class="sxs-lookup"><span data-stu-id="bcd5b-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="bcd5b-195">Изменение кода компонента</span><span class="sxs-lookup"><span data-stu-id="bcd5b-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="bcd5b-196">Что произойдет, если правила компонентов будут разорваны?</span><span class="sxs-lookup"><span data-stu-id="bcd5b-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="bcd5b-197">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-198">Используйте сторонние установщик Windows средства разработки пакетов или средства пакета SDK, такие как [Orca.exe](orca-exe.md) для заполнения базы данных установки и создания пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="bcd5b-199">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-200">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="bcd5b-201">Пакет установки, сведения о базе данных установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="bcd5b-202">установщик Windows расширения файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="bcd5b-203">Таблицы базы данных</span><span class="sxs-lookup"><span data-stu-id="bcd5b-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="bcd5b-204">Коды пакетов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="bcd5b-205">Создание большого пакета</span><span class="sxs-lookup"><span data-stu-id="bcd5b-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="bcd5b-206">Установщик Windows в 64-разрядных операционных системах</span><span class="sxs-lookup"><span data-stu-id="bcd5b-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="bcd5b-207">Именование настраиваемых таблиц, свойств и действий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="bcd5b-208">Ограничения для потоков OLE</span><span class="sxs-lookup"><span data-stu-id="bcd5b-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="bcd5b-209">Формат определения столбца</span><span class="sxs-lookup"><span data-stu-id="bcd5b-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="bcd5b-210">Уменьшение размера MSI файла</span><span class="sxs-lookup"><span data-stu-id="bcd5b-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="bcd5b-211">Создайте базу данных установщик Windows для установки файлов.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="bcd5b-212">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-213">Группа основных таблиц</span><span class="sxs-lookup"><span data-stu-id="bcd5b-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="bcd5b-214">Группа таблиц файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="bcd5b-215">Таблица файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="bcd5b-216">Поиск файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="bcd5b-217">Стоимость файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="bcd5b-218">Установка файла</span><span class="sxs-lookup"><span data-stu-id="bcd5b-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="bcd5b-219">Сопутствующие файлы</span><span class="sxs-lookup"><span data-stu-id="bcd5b-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="bcd5b-220">Правила управления версиями файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="bcd5b-221">Управление версиями файлов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bcd5b-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="bcd5b-222">Замена существующих файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="bcd5b-223">Использование ящиков и сжатых источников</span><span class="sxs-lookup"><span data-stu-id="bcd5b-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="bcd5b-224">Удаление потерянных файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="bcd5b-225">Установка постоянных компонентов, файлов, шрифтов, разделов реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="bcd5b-226">Таблица Филесфпкаталог</span><span class="sxs-lookup"><span data-stu-id="bcd5b-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="bcd5b-227">Поиск файла и создание свойства, содержащего путь к файлу</span><span class="sxs-lookup"><span data-stu-id="bcd5b-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="bcd5b-228">Поиск каталога и файла в каталоге</span><span class="sxs-lookup"><span data-stu-id="bcd5b-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="bcd5b-229">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-230">Создание установщик Windows базы данных, которая устанавливает структуру каталогов и папки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="bcd5b-231">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-232">Группа основных таблиц</span><span class="sxs-lookup"><span data-stu-id="bcd5b-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="bcd5b-233">Группа таблиц файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="bcd5b-234">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="bcd5b-235">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="bcd5b-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="bcd5b-236">Использование таблицы Directory</span><span class="sxs-lookup"><span data-stu-id="bcd5b-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="bcd5b-237">Использование свойства каталога в пути</span><span class="sxs-lookup"><span data-stu-id="bcd5b-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="bcd5b-238">Свойства системной папки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="bcd5b-239">Таблица Креатефолдер</span><span class="sxs-lookup"><span data-stu-id="bcd5b-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="bcd5b-240">Таблица Локкпермиссионс</span><span class="sxs-lookup"><span data-stu-id="bcd5b-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="bcd5b-241">Таблица Мсилоккпермиссионсекс</span><span class="sxs-lookup"><span data-stu-id="bcd5b-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="bcd5b-242">Изменение целевого расположения каталога</span><span class="sxs-lookup"><span data-stu-id="bcd5b-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="bcd5b-243">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-244">Создайте базу данных установщик Windows, которая устанавливает разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="bcd5b-245">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-246">Группа основных таблиц</span><span class="sxs-lookup"><span data-stu-id="bcd5b-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="bcd5b-247">Группа таблиц реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="bcd5b-248">Таблица реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="bcd5b-249">Изменение реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="bcd5b-250">Добавление или удаление разделов реестра при установке или удалении компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="bcd5b-251">Добавление и удаление приложения без трассировки в реестре</span><span class="sxs-lookup"><span data-stu-id="bcd5b-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="bcd5b-252">Установка постоянных компонентов, файлов, шрифтов, разделов реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="bcd5b-253">Поиск существующих приложений, файлов, записей реестра или INI-файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="bcd5b-254">Поиск записи реестра и создание свойства, содержащего значение реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="bcd5b-255">Разделы реестра сборки, записанные установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="bcd5b-256">Удалить раздел реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="bcd5b-257">Таблица Селфрег</span><span class="sxs-lookup"><span data-stu-id="bcd5b-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="bcd5b-258">Указание порядка самостоятельной регистрации</span><span class="sxs-lookup"><span data-stu-id="bcd5b-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="bcd5b-259">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-260">Создание установщик Windows базы данных, которая устанавливает службы.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="bcd5b-261">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-262">Таблица Сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="bcd5b-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="bcd5b-263">Таблица ServiceControl</span><span class="sxs-lookup"><span data-stu-id="bcd5b-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="bcd5b-264">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="bcd5b-265">Создайте базу данных установщик Windows, которая устанавливает изолированные компоненты или компоненты COM.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="bcd5b-266">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-267">Группа таблиц реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="bcd5b-268">Таблица классов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="bcd5b-269">Таблица ComPlus</span><span class="sxs-lookup"><span data-stu-id="bcd5b-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="bcd5b-270">Изолированные компоненты</span><span class="sxs-lookup"><span data-stu-id="bcd5b-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="bcd5b-271">Использование изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="bcd5b-272">Установка изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="bcd5b-273">Повторная установка изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="bcd5b-274">Удаление изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="bcd5b-275">Установка COM-компонента в Закрытое расположение</span><span class="sxs-lookup"><span data-stu-id="bcd5b-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="bcd5b-276">Сделать компонент COM в существующем пакете частным</span><span class="sxs-lookup"><span data-stu-id="bcd5b-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="bcd5b-277">Установка приложения COM+ с установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="bcd5b-278">Установка компонента, не являющегося компонентом COM, в Закрытое расположение</span><span class="sxs-lookup"><span data-stu-id="bcd5b-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="bcd5b-279">Создание частного компонента, не являющегося компонентом COM, в существующем пакете</span><span class="sxs-lookup"><span data-stu-id="bcd5b-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="bcd5b-280">Создание установщик Windows базы данных, которая устанавливает сборки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="bcd5b-281">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-282">Таблица Мсиассембли</span><span class="sxs-lookup"><span data-stu-id="bcd5b-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="bcd5b-283">Таблица Мсиассемблинаме</span><span class="sxs-lookup"><span data-stu-id="bcd5b-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="bcd5b-284">Сборки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="bcd5b-285">Разделы реестра сборки, записанные установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="bcd5b-286">Установка сборок Win32</span><span class="sxs-lookup"><span data-stu-id="bcd5b-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="bcd5b-287">Создайте базу данных установщик Windows, которая устанавливает драйверы и трансляторы ODBC.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="bcd5b-288">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-289">Таблица Одбкаттрибуте</span><span class="sxs-lookup"><span data-stu-id="bcd5b-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="bcd5b-290">Таблица Одбкдривер</span><span class="sxs-lookup"><span data-stu-id="bcd5b-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="bcd5b-291">Таблица Одбктранслатор</span><span class="sxs-lookup"><span data-stu-id="bcd5b-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="bcd5b-292">Таблица Одбкдатасаурце</span><span class="sxs-lookup"><span data-stu-id="bcd5b-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="bcd5b-293">Таблица Одбксаурцеаттрибуте</span><span class="sxs-lookup"><span data-stu-id="bcd5b-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="bcd5b-294">Создание установщик Windows базы данных, которая устанавливает MIME.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="bcd5b-295">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-296">Таблица MIME</span><span class="sxs-lookup"><span data-stu-id="bcd5b-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="bcd5b-297">Таблица расширения</span><span class="sxs-lookup"><span data-stu-id="bcd5b-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="bcd5b-298">Изменение реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="bcd5b-299">Создайте базу данных установщик Windows, которая устанавливает переменные среды.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="bcd5b-300">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-301">Таблица среды</span><span class="sxs-lookup"><span data-stu-id="bcd5b-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="bcd5b-302">Создание установщик Windows базы данных, которая устанавливает ярлыки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="bcd5b-303">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-304">Таблица ярлыков</span><span class="sxs-lookup"><span data-stu-id="bcd5b-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="bcd5b-305">Таблица Мсишорткутпроперти</span><span class="sxs-lookup"><span data-stu-id="bcd5b-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="bcd5b-306">Изменение ярлыков установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="bcd5b-307">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-308">Создание установщик Windows базы данных, которая устанавливает несколько экземпляров приложений.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="bcd5b-309">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-310">Установка нескольких экземпляров продуктов и исправлений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="bcd5b-311">Создание нескольких экземпляров с помощью преобразований экземпляров</span><span class="sxs-lookup"><span data-stu-id="bcd5b-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="bcd5b-312">Установка нескольких экземпляров с преобразованиями экземпляров</span><span class="sxs-lookup"><span data-stu-id="bcd5b-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="bcd5b-313">Укажите состояния и параметры выбора компонентов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="bcd5b-314">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-315">Группа основных таблиц</span><span class="sxs-lookup"><span data-stu-id="bcd5b-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="bcd5b-316">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="bcd5b-317">Таблица функций</span><span class="sxs-lookup"><span data-stu-id="bcd5b-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="bcd5b-318">Таблица Феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="bcd5b-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="bcd5b-319">Управление состояниями выбора компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="bcd5b-320">Свойства параметров установки компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="bcd5b-321">Укажите условия, которые должны быть удовлетворены для установки приложения или выбранных компонентов.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="bcd5b-322">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-323">Таблица условий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="bcd5b-324">Таблица Лаунчкондитион</span><span class="sxs-lookup"><span data-stu-id="bcd5b-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="bcd5b-325">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="bcd5b-326">Использование свойств в условных инструкциях</span><span class="sxs-lookup"><span data-stu-id="bcd5b-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="bcd5b-327">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="bcd5b-328">Действия по обработке условий, выполняемые во время удаления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="bcd5b-329">Примеры синтаксиса условных операторов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="bcd5b-330">Создайте последовательность действий, используемых для установки приложения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="bcd5b-331">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-332">Использование таблицы последовательностей</span><span class="sxs-lookup"><span data-stu-id="bcd5b-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="bcd5b-333">Группа таблиц процедур установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="bcd5b-334">Подробный пример таблицы последовательности</span><span class="sxs-lookup"><span data-stu-id="bcd5b-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="bcd5b-335">Действия с ограничениями последовательности</span><span class="sxs-lookup"><span data-stu-id="bcd5b-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="bcd5b-336">Действия без ограничений на последовательность</span><span class="sxs-lookup"><span data-stu-id="bcd5b-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="bcd5b-337">Использование свойств в условных инструкциях</span><span class="sxs-lookup"><span data-stu-id="bcd5b-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="bcd5b-338">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="bcd5b-339">Примеры синтаксиса условных операторов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="bcd5b-340">Действия по обработке условий, выполняемые во время удаления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="bcd5b-341">Стандартные действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="bcd5b-342">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-343">Подготовьте пакет установки приложения для будущих обновлений приложения с помощью службы установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="bcd5b-344">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-345">Установка исправлений и обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="bcd5b-346">Подготовка приложения к будущим основным обновлениям</span><span class="sxs-lookup"><span data-stu-id="bcd5b-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="bcd5b-347">Использование UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="bcd5b-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="bcd5b-348">Обновление таблицы</span><span class="sxs-lookup"><span data-stu-id="bcd5b-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="bcd5b-349">**UpgradeCode, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="bcd5b-350">Предотвращение установки старого пакета более новой версией</span><span class="sxs-lookup"><span data-stu-id="bcd5b-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="bcd5b-351">Изменение кода продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="bcd5b-352">Обновление сборок</span><span class="sxs-lookup"><span data-stu-id="bcd5b-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="bcd5b-353">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="bcd5b-354">Устранение неполадок установщик Windows пакетов в процессе разработки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="bcd5b-355">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-356">Проверка пакета</span><span class="sxs-lookup"><span data-stu-id="bcd5b-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="bcd5b-357">Внутренние средства оценки согласованности — ICEs</span><span class="sxs-lookup"><span data-stu-id="bcd5b-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="bcd5b-358">Ведение журнала установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="bcd5b-359">Проверка установки компонентов, компонентов, файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="bcd5b-360">Создание большого пакета</span><span class="sxs-lookup"><span data-stu-id="bcd5b-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="bcd5b-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="bcd5b-362">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="bcd5b-363">Проверка модулей слияния</span><span class="sxs-lookup"><span data-stu-id="bcd5b-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="bcd5b-364">Проверка базы данных установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="bcd5b-365">Проверка обновления установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="bcd5b-366">Поиск неработающей функции или компонента</span><span class="sxs-lookup"><span data-stu-id="bcd5b-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="bcd5b-367">установщик Windows сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="bcd5b-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="bcd5b-368">Ведение журнала запросов на перезагрузку</span><span class="sxs-lookup"><span data-stu-id="bcd5b-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="bcd5b-369">Обеспечьте безопасную установку и установку приложения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="bcd5b-370">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-371">Рекомендации по созданию безопасных установок</span><span class="sxs-lookup"><span data-stu-id="bcd5b-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="bcd5b-372">Рекомендации по защите настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="bcd5b-373">Безопасность настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="bcd5b-374">Рекомендации по защите пакетов на заблокированных компьютерах</span><span class="sxs-lookup"><span data-stu-id="bcd5b-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="bcd5b-375">Создание полностью проверенной подписанной установки с помощью службы автоматизации</span><span class="sxs-lookup"><span data-stu-id="bcd5b-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="bcd5b-376">Пример установки с применением установщика на базе URL</span><span class="sxs-lookup"><span data-stu-id="bcd5b-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="bcd5b-377">Создание пользовательского интерфейса для ввода пароля</span><span class="sxs-lookup"><span data-stu-id="bcd5b-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="bcd5b-378">Цифровые подписи и установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="bcd5b-379">Использование установщик Windows с UAC</span><span class="sxs-lookup"><span data-stu-id="bcd5b-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="bcd5b-380">Исправление контроля учетных записей пользователей (UAC)</span><span class="sxs-lookup"><span data-stu-id="bcd5b-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="bcd5b-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="bcd5b-382">**AdminUser, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="bcd5b-383">**Привилегированное свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="bcd5b-384">**Секурекустомпропертиес, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="bcd5b-385">Создайте пользовательский интерфейс для отображения параметров для настройки установки и получения сведений от пользователя о ожидающем процессе установки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="bcd5b-386">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-387">Сведения о пользовательском интерфейсе</span><span class="sxs-lookup"><span data-stu-id="bcd5b-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="bcd5b-388">Добавление элементов управления и текста</span><span class="sxs-lookup"><span data-stu-id="bcd5b-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="bcd5b-389">Создание элемента управления ProgressBar</span><span class="sxs-lookup"><span data-stu-id="bcd5b-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="bcd5b-390">Создание сообщений с приглашением на диск</span><span class="sxs-lookup"><span data-stu-id="bcd5b-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="bcd5b-391">Создание условного выражения "Подождите..." Окно сообщения</span><span class="sxs-lookup"><span data-stu-id="bcd5b-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="bcd5b-392">Предварительный просмотр пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bcd5b-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="bcd5b-393">Добавление текста, хранящегося в свойстве</span><span class="sxs-lookup"><span data-stu-id="bcd5b-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="bcd5b-394">**мсисетинтерналуи**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="bcd5b-395">Создайте внешний пользовательский интерфейс, чтобы предоставить настраиваемый пользовательский интерфейс для настройки установки и получения от пользователя сведений о ожидающем процессе установки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="bcd5b-396">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-397">**мсисетекстерналуи**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="bcd5b-398">Мониторинг установки с помощью Мсисетекстерналуирекорд</span><span class="sxs-lookup"><span data-stu-id="bcd5b-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="bcd5b-399">Синтаксический анализ сообщений установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="bcd5b-400">Возвращение значений из внешнего обработчика пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bcd5b-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="bcd5b-401">\_обработчик инсталлуи</span><span class="sxs-lookup"><span data-stu-id="bcd5b-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="bcd5b-402">Обработка сообщений о ходе выполнения с помощью Мсисетекстерналуи</span><span class="sxs-lookup"><span data-stu-id="bcd5b-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="bcd5b-403">Мониторинг установки с помощью Мсисетекстерналуи</span><span class="sxs-lookup"><span data-stu-id="bcd5b-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="bcd5b-404">Задание сведений для приложения в окне " **Установка и удаление программ** " (ARP)</span><span class="sxs-lookup"><span data-stu-id="bcd5b-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="bcd5b-405">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-406">Настройка установки и удаления программ с помощью установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="bcd5b-407">Добавление и удаление приложения без трассировки в реестре</span><span class="sxs-lookup"><span data-stu-id="bcd5b-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="bcd5b-408">Удалить раздел реестра</span><span class="sxs-lookup"><span data-stu-id="bcd5b-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="bcd5b-409">Создание настраиваемых действий для обработки логики установки, которая изначально не поддерживается установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="bcd5b-410">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-411">Настраиваемые действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="bcd5b-412">Сводный список всех типов настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="bcd5b-413">Рекомендации по защите настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="bcd5b-414">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="bcd5b-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="bcd5b-415">Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="bcd5b-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="bcd5b-416">Использование настраиваемого действия для запуска установленного файла в конце установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="bcd5b-417">Доступ к базе данных или сеансу из настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="bcd5b-418">Доступ к текущему сеансу установщика из пользовательского действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="bcd5b-419">Изменение состояния системы с помощью настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="bcd5b-420">Начальная загрузка установщик Windows на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="bcd5b-421">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-422">Начальной загрузки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="bcd5b-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="bcd5b-424">Начальная загрузка со скачиванием из Интернета</span><span class="sxs-lookup"><span data-stu-id="bcd5b-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="bcd5b-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="bcd5b-426">Пример установки с применением установщика на базе URL</span><span class="sxs-lookup"><span data-stu-id="bcd5b-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="bcd5b-427">Настройка ресурсов Setup.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="bcd5b-428">Загрузка установки из Интернета</span><span class="sxs-lookup"><span data-stu-id="bcd5b-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="bcd5b-429">Придерживайтесь Active Accessibility рекомендаций при написании пакетов установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="bcd5b-430">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-431">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="bcd5b-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="bcd5b-432">Подготовьтесь к международной настройке приложения.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="bcd5b-433">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="bcd5b-434">[Подготовка пакета установщик Windows для локализации](preparing-a-windows-installer-package-for-localization.md),</span><span class="sxs-lookup"><span data-stu-id="bcd5b-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="bcd5b-435">Локализация пакета установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="bcd5b-436">Обработка кодовой страницы (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="bcd5b-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="bcd5b-437">Добавление локализованных ресурсов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="bcd5b-438">Пример локализации</span><span class="sxs-lookup"><span data-stu-id="bcd5b-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="bcd5b-439">Локализация таблиц ошибок и Актионтекст</span><span class="sxs-lookup"><span data-stu-id="bcd5b-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="bcd5b-440">Локализация столбцов базы данных</span><span class="sxs-lookup"><span data-stu-id="bcd5b-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="bcd5b-441">Создание базы данных со нейтральной кодовой страницей</span><span class="sxs-lookup"><span data-stu-id="bcd5b-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="bcd5b-442">Обработка кодовой страницы импортированных и экспортированных таблиц</span><span class="sxs-lookup"><span data-stu-id="bcd5b-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="bcd5b-443">Локализация языка, отображаемого диалоговыми окнами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="bcd5b-444">Импорт локализованных таблиц ошибок и Актионтекст</span><span class="sxs-lookup"><span data-stu-id="bcd5b-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="bcd5b-445">Обновление свойств Продуктлангуаже и ProductCode</span><span class="sxs-lookup"><span data-stu-id="bcd5b-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="bcd5b-446">Обновление потока сводных данных</span><span class="sxs-lookup"><span data-stu-id="bcd5b-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="bcd5b-447">Компоненты с квалификаторами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="bcd5b-448">Таблица Уитекст</span><span class="sxs-lookup"><span data-stu-id="bcd5b-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="bcd5b-449">Управление языком и кодовой страницей</span><span class="sxs-lookup"><span data-stu-id="bcd5b-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="bcd5b-450">Проверка кодовой страницы базы данных установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="bcd5b-451">Создание пакетов установщик Windows для 32-разрядных и 64-разрядных платформ.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="bcd5b-452">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-453">Установщик Windows в 64-разрядных операционных системах</span><span class="sxs-lookup"><span data-stu-id="bcd5b-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="bcd5b-454">64-разрядные пользовательские действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="bcd5b-455">Использование 64-разрядных настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="bcd5b-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="bcd5b-456">Использование 64-разрядных модулей слияния</span><span class="sxs-lookup"><span data-stu-id="bcd5b-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="bcd5b-457">Распространение общих компонентов установщик Windows и логики установки в виде модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="bcd5b-458">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-459">Модули слияния</span><span class="sxs-lookup"><span data-stu-id="bcd5b-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="bcd5b-460">Создание языкового преобразования для модуля многоязычного слияния</span><span class="sxs-lookup"><span data-stu-id="bcd5b-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="bcd5b-461">Применение настраиваемого модуля слияния с настройками</span><span class="sxs-lookup"><span data-stu-id="bcd5b-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="bcd5b-462">Запланируйте или подавление перезагрузок во время установки установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="bcd5b-463">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-464">Перезагрузка системы</span><span class="sxs-lookup"><span data-stu-id="bcd5b-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="bcd5b-465">Ведение журнала запросов на перезагрузку</span><span class="sxs-lookup"><span data-stu-id="bcd5b-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="bcd5b-466">Создание обновлений или исправлений для существующего приложения путем создания исправления.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="bcd5b-467">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-468">Создание небольшого исправления обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="bcd5b-469">Пример небольшого обновления исправлений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="bcd5b-470">Создайте пакет с двойным набором, поддерживающий установку приложения либо только для текущего пользователя, либо для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="bcd5b-471">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-472">Контекст установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="bcd5b-473">Создание отдельных пакетов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="bcd5b-474">Пример создания отдельного пакета</span><span class="sxs-lookup"><span data-stu-id="bcd5b-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="bcd5b-475">Настройка служб на компьютере с помощью установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="bcd5b-476">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-477">Использование конфигурации служб</span><span class="sxs-lookup"><span data-stu-id="bcd5b-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="bcd5b-478">Защита ресурсов на компьютере с помощью установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="bcd5b-479">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-480">Рекомендации по созданию безопасных установок</span><span class="sxs-lookup"><span data-stu-id="bcd5b-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="bcd5b-481">Защита ресурсов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="bcd5b-482">Перечисление всех компонентов, установленных на компьютере, и получение пути к ключу для компонента.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="bcd5b-483">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-484">Перечисление компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="bcd5b-485">Установка нескольких пакетов с помощью [*обработки транзакций*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bcd5b-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="bcd5b-486">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-487">Установки с несколькими пакетами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="bcd5b-488">Внедрение настраиваемого пользовательского интерфейса в пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="bcd5b-489">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-490">Использование пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bcd5b-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="bcd5b-491">Использование встроенного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bcd5b-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="bcd5b-492">ИТ-специалисты</span><span class="sxs-lookup"><span data-stu-id="bcd5b-492">IT Professionals</span></span>

<span data-ttu-id="bcd5b-493">ИТ-специалисты и администраторы настраивают и развертывают существующие пакеты установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="bcd5b-494">Эти пользователи переупаковывают программы установки для существующих приложений в установщик Windows пакеты установки, а затем устанавливают и обслуживают административные образы установок установщик Windows в сетях.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="bcd5b-495">Настройка приложений и настроек с помощью создания и применения преобразований установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="bcd5b-496">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-497">Настройка</span><span class="sxs-lookup"><span data-stu-id="bcd5b-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="bcd5b-498">Преобразования баз данных</span><span class="sxs-lookup"><span data-stu-id="bcd5b-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="bcd5b-499">Пример преобразования настройки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="bcd5b-500">Слияния и преобразования</span><span class="sxs-lookup"><span data-stu-id="bcd5b-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="bcd5b-501">Использование преобразований для добавления ресурсов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="bcd5b-502">Создание преобразования</span><span class="sxs-lookup"><span data-stu-id="bcd5b-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="bcd5b-503">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="bcd5b-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="bcd5b-505">Применение преобразования</span><span class="sxs-lookup"><span data-stu-id="bcd5b-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="bcd5b-506">Просмотр преобразования</span><span class="sxs-lookup"><span data-stu-id="bcd5b-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="bcd5b-507">Просмотр различий между двумя базами данных</span><span class="sxs-lookup"><span data-stu-id="bcd5b-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="bcd5b-508">Исправление настроенных приложений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="bcd5b-509">Развертывание пакета установки установщик Windows, обновления или исправления.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="bcd5b-510">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-511">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="bcd5b-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="bcd5b-512">Установка исправлений и обновления</span><span class="sxs-lookup"><span data-stu-id="bcd5b-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="bcd5b-513">Преобразования</span><span class="sxs-lookup"><span data-stu-id="bcd5b-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="bcd5b-514">Установка пакета с повышенными привилегиями для без прав администратора</span><span class="sxs-lookup"><span data-stu-id="bcd5b-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="bcd5b-515">Применение основных обновлений путем исправления локальной установки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="bcd5b-516">Применение основных обновлений путем установки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="bcd5b-517">Применение небольших обновлений путем исправления локальной установки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="bcd5b-518">Применение небольших обновлений путем переустановки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="bcd5b-519">Применение небольших обновлений путем исправления административного образа</span><span class="sxs-lookup"><span data-stu-id="bcd5b-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="bcd5b-520">Установка исправлений первоначальных установок</span><span class="sxs-lookup"><span data-stu-id="bcd5b-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="bcd5b-521">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="bcd5b-522">Устранение неполадок установщик Windows пакетов.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="bcd5b-523">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-524">Ведение журнала установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="bcd5b-525">Проверка установки компонентов, компонентов, файлов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="bcd5b-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="bcd5b-527">Поиск неработающей функции или компонента</span><span class="sxs-lookup"><span data-stu-id="bcd5b-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="bcd5b-528">установщик Windows сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="bcd5b-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="bcd5b-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="bcd5b-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="bcd5b-530">Используйте скрипты для запроса пакетов установщик Windows для получения сведений о продукте и изменения установки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="bcd5b-531">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-532">Интерфейс автоматизации</span><span class="sxs-lookup"><span data-stu-id="bcd5b-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="bcd5b-533">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcd5b-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="bcd5b-534">Использование установщик Windows с WMI</span><span class="sxs-lookup"><span data-stu-id="bcd5b-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="bcd5b-535">Создание и обслуживание административных установок.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="bcd5b-536">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-537">Административная установка</span><span class="sxs-lookup"><span data-stu-id="bcd5b-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="bcd5b-538">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="bcd5b-539">**Админпропертиес, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="bcd5b-540">Применение небольших обновлений путем исправления административного образа</span><span class="sxs-lookup"><span data-stu-id="bcd5b-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="bcd5b-541">Применение пакета исправлений к административной установке</span><span class="sxs-lookup"><span data-stu-id="bcd5b-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="bcd5b-542">Порядок выполнения действия</span><span class="sxs-lookup"><span data-stu-id="bcd5b-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="bcd5b-543">**Исадминпаккаже, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="bcd5b-544">Порядок приоритета свойств</span><span class="sxs-lookup"><span data-stu-id="bcd5b-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="bcd5b-545">**Админпропертиес, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="bcd5b-546">Сделать приложение доступным только для всех пользователей компьютера или только для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="bcd5b-547">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-548">Контекст установки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="bcd5b-549">**Свойство ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="bcd5b-550">Анализ пакетов, установка продуктов и Настройка параметров функций с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="bcd5b-551">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-552">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="bcd5b-553">Установка значений открытых свойств в командной строке</span><span class="sxs-lookup"><span data-stu-id="bcd5b-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="bcd5b-554">Получение и задание свойств</span><span class="sxs-lookup"><span data-stu-id="bcd5b-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="bcd5b-555">Переустановка компонента или приложения</span><span class="sxs-lookup"><span data-stu-id="bcd5b-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="bcd5b-556">Применение небольших обновлений путем исправления локальной установки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="bcd5b-557">Применение небольших обновлений путем переустановки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="bcd5b-558">Изменение целевого расположения каталога</span><span class="sxs-lookup"><span data-stu-id="bcd5b-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="bcd5b-559">Применение небольших обновлений путем исправления административного образа</span><span class="sxs-lookup"><span data-stu-id="bcd5b-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="bcd5b-560">Применение основных обновлений путем установки продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="bcd5b-561">Свойства конфигурации</span><span class="sxs-lookup"><span data-stu-id="bcd5b-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="bcd5b-562">Свойства параметров установки компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="bcd5b-563">Работа с политикой для управления правами доступа и разрешениями.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="bcd5b-564">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="bcd5b-565">[Политики компьютера](machine-policies.md),</span><span class="sxs-lookup"><span data-stu-id="bcd5b-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="bcd5b-566">[Политики пользователя](user-policies.md),</span><span class="sxs-lookup"><span data-stu-id="bcd5b-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="bcd5b-567">Установка пакета с повышенными привилегиями для без прав администратора</span><span class="sxs-lookup"><span data-stu-id="bcd5b-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="bcd5b-568">Объявление приложения Per-User для установки с повышенными привилегиями</span><span class="sxs-lookup"><span data-stu-id="bcd5b-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="bcd5b-569">Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="bcd5b-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="bcd5b-570">**AdminUser, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="bcd5b-571">**Привилегированное свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="bcd5b-572">**Енаблеусерконтрол, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="bcd5b-573">**Свойство "значение"**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="bcd5b-574">**Секурекустомпропертиес, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="bcd5b-575">Установка нескольких пакетов с помощью [*обработки транзакций*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bcd5b-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="bcd5b-576">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-577">Установки с несколькими пакетами</span><span class="sxs-lookup"><span data-stu-id="bcd5b-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="bcd5b-578">Внедрение настраиваемого пользовательского интерфейса в пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="bcd5b-579">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-580">Использование пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bcd5b-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="bcd5b-581">Использование встроенного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bcd5b-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="bcd5b-582">Разработчики инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="bcd5b-582">Infrastructure Developers</span></span>

<span data-ttu-id="bcd5b-583">Разработчики инфраструктуры могут создавать унифицированные платформы для развертывания программного обеспечения, использующего службу установщик Windows, и управления им.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="bcd5b-584">Они могут использовать программный интерфейс установщик Windows для запроса, управления и распространения приложений, исправлений и источников в системе.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="bcd5b-585">Поиск, Инвентаризация и запрос сведений о состоянии, информации и клиентах компонентов.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="bcd5b-586">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-587">Функции для конкретных компонентов</span><span class="sxs-lookup"><span data-stu-id="bcd5b-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-588">Функции состояния системы</span><span class="sxs-lookup"><span data-stu-id="bcd5b-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-589">Объект установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="bcd5b-590">Объект Product</span><span class="sxs-lookup"><span data-stu-id="bcd5b-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="bcd5b-591">Объект Patch</span><span class="sxs-lookup"><span data-stu-id="bcd5b-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="bcd5b-592">Инвентаризация и запрос информации и состояния продуктов и функций.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="bcd5b-593">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-594">Инвентаризация продуктов и исправлений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="bcd5b-595">Функции состояния системы</span><span class="sxs-lookup"><span data-stu-id="bcd5b-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-596">Функции запроса продукта</span><span class="sxs-lookup"><span data-stu-id="bcd5b-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-597">Объект установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="bcd5b-598">Объект Product</span><span class="sxs-lookup"><span data-stu-id="bcd5b-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="bcd5b-599">Объект Patch</span><span class="sxs-lookup"><span data-stu-id="bcd5b-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="bcd5b-600">Повышение устойчивости источника с помощью установщик Windows для инвентаризации, запроса и изменения исходного списка приложений, обновлений и исправлений.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="bcd5b-601">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-602">**Свойство SOURCELIST**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="bcd5b-603">**Отказоустойчивость источника**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="bcd5b-604">Функции установки и настройки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-605">Объект установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="bcd5b-606">Объект Product</span><span class="sxs-lookup"><span data-stu-id="bcd5b-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="bcd5b-607">Объект Patch</span><span class="sxs-lookup"><span data-stu-id="bcd5b-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="bcd5b-608">Повышение отказоустойчивости источника с помощью установщик Windows для инвентаризации, запроса и изменения источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="bcd5b-609">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-610">**Свойство SOURCELIST**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="bcd5b-611">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="bcd5b-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="bcd5b-612">Функции установки и настройки</span><span class="sxs-lookup"><span data-stu-id="bcd5b-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-613">Объект Product</span><span class="sxs-lookup"><span data-stu-id="bcd5b-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="bcd5b-614">Объект Patch</span><span class="sxs-lookup"><span data-stu-id="bcd5b-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="bcd5b-615">Инвентаризация и запрос информации и состояния исправлений.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="bcd5b-616">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-617">Инвентаризация продуктов и исправлений</span><span class="sxs-lookup"><span data-stu-id="bcd5b-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="bcd5b-618">Справочник по функциям установщика</span><span class="sxs-lookup"><span data-stu-id="bcd5b-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="bcd5b-619">Объект Patch</span><span class="sxs-lookup"><span data-stu-id="bcd5b-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="bcd5b-620">Работа с политикой для управления правами доступа и разрешениями.</span><span class="sxs-lookup"><span data-stu-id="bcd5b-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="bcd5b-621">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bcd5b-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="bcd5b-622">Политики компьютера</span><span class="sxs-lookup"><span data-stu-id="bcd5b-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="bcd5b-623">Политики пользователя</span><span class="sxs-lookup"><span data-stu-id="bcd5b-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="bcd5b-624">Установка пакета с повышенными привилегиями для без прав администратора</span><span class="sxs-lookup"><span data-stu-id="bcd5b-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="bcd5b-625">Объявление приложения Per-User для установки с повышенными привилегиями</span><span class="sxs-lookup"><span data-stu-id="bcd5b-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="bcd5b-626">Использование настраиваемого действия для создания учетных записей пользователей на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="bcd5b-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="bcd5b-627">**AdminUser, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="bcd5b-628">**Привилегированное свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="bcd5b-629">**Енаблеусерконтрол, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="bcd5b-630">**Свойство "значение"**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="bcd5b-631">**Секурекустомпропертиес, свойство**</span><span class="sxs-lookup"><span data-stu-id="bcd5b-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



