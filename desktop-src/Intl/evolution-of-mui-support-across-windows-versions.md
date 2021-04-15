---
description: Развитие поддержки многоязыкового интерфейса пользователя в разных версиях Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Развитие поддержки многоязыкового интерфейса пользователя в разных версиях Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683678"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="26312-103">Развитие поддержки многоязыкового интерфейса пользователя в разных версиях Windows</span><span class="sxs-lookup"><span data-stu-id="26312-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="26312-104">До Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26312-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="26312-105">Windows Vista и более поздние</span><span class="sxs-lookup"><span data-stu-id="26312-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="26312-106">Операционная система, не зависящая от языка/MUI</span><span class="sxs-lookup"><span data-stu-id="26312-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="26312-107">Сценарии развертывания — это полностью основанный на многоязыковых интерфейсах</span><span class="sxs-lookup"><span data-stu-id="26312-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="26312-108">Развертывание одного образа</span><span class="sxs-lookup"><span data-stu-id="26312-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="26312-109">Улучшенная модель обслуживания</span><span class="sxs-lookup"><span data-stu-id="26312-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="26312-110">Инфраструктура многоязыкового интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="26312-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="26312-111">Управление языками</span><span class="sxs-lookup"><span data-stu-id="26312-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="26312-112">Обработка ресурсов</span><span class="sxs-lookup"><span data-stu-id="26312-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="26312-113">До Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26312-113">Before Windows Vista</span></span>

<span data-ttu-id="26312-114">До выпуска Windows Vista Windows поставляется с одноязыковыми образами, которые означали, что Каждая локализованная версия Windows содержала один язык для своего пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26312-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="26312-115">MUI был надстройкой для английской версии операционной системы, а пакеты многоязыкового интерфейса пользователя можно было добавлять только в определенные английские версии Windows.</span><span class="sxs-lookup"><span data-stu-id="26312-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="26312-116">При установке в английской версии Windows MUI может изменить язык пользовательского интерфейса операционной системы в соответствии с предпочтениями отдельных пользователей на один из поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="26312-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="26312-117">Модель пакета MUI не предоставляла поддержку MUI для приложений.</span><span class="sxs-lookup"><span data-stu-id="26312-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="26312-118">Хотя разработчики могут создавать многоязыковые приложения, им пришлось создавать собственные механизмы для этого.</span><span class="sxs-lookup"><span data-stu-id="26312-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="26312-119">Windows Vista и более поздние</span><span class="sxs-lookup"><span data-stu-id="26312-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="26312-120">В Windows Vista корпорация Майкрософт внесла значительные инвестиции в MUI.</span><span class="sxs-lookup"><span data-stu-id="26312-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="26312-121">Windows Vista построена с нуля на платформе MUI.</span><span class="sxs-lookup"><span data-stu-id="26312-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="26312-122">Хотя это и является основной стратегией в стратегии локализации Windows, так как она является ключевым средством, которое позволяет корпорации Майкрософт предоставлять Windows на более языках, чем когда-либо ранее, это первое и самое главное для пользователей и клиентов Windows.</span><span class="sxs-lookup"><span data-stu-id="26312-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="26312-123">Операционная система, не зависящая от языка/MUI</span><span class="sxs-lookup"><span data-stu-id="26312-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="26312-124">Большинство двоичных файлов Windows Vista совместимо с MUI, и их локализуемые данные хранятся отдельно от кода.</span><span class="sxs-lookup"><span data-stu-id="26312-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="26312-125">Это обеспечивает гибкость, поскольку в любое время можно добавлять различные языковые данные.</span><span class="sxs-lookup"><span data-stu-id="26312-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="26312-126">Сценарии развертывания — это полностью основанный на многоязыковых интерфейсах</span><span class="sxs-lookup"><span data-stu-id="26312-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="26312-127">Архитектура упаковки и установки Windows Vista основана на многоязычном интерфейсе пользователя, и все локализуемые данные упаковываются в пакеты для конкретных языков, а каждый языковой пакет может быть развернут в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="26312-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="26312-128">Например, несмотря на то, что розничные DVD-диски для Windows Vista содержат одноязыковые версии, пользователи выпуска Ultimate могут загружать дополнительные языковые пакеты MUI и могут переключать язык пользовательского интерфейса с панели управления " **язык и региональные стандарты** ".</span><span class="sxs-lookup"><span data-stu-id="26312-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="26312-129">Лицензии Enterprise Edition получают все языки и могут развертывать их.</span><span class="sxs-lookup"><span data-stu-id="26312-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="26312-130">Развертывание одного образа</span><span class="sxs-lookup"><span data-stu-id="26312-130">Single image deployment</span></span>

<span data-ttu-id="26312-131">Корпоративные клиенты и поставщики вычислительной техники теперь могут сократить количество образов, которые необходимо поддерживать, чтобы развертывать Windows и приложения на компьютерах в разных языковых стандартах с помощью развертывания одного образа.</span><span class="sxs-lookup"><span data-stu-id="26312-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="26312-132">При использовании многоязыкового интерфейса пользователя в Windows Vista один образ, содержащий несколько языков, может быть развернут для пользователей любого языка, и пользователи могут определить собственные предпочитаемые языки (в рамках политики) во время установки или начальную версию "без рамки" на компьютере.</span><span class="sxs-lookup"><span data-stu-id="26312-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="26312-133">В частности, поставщики вычислительной техники могут разместить на новых компьютерах множество языков интерфейса пользователя, чтобы пользователи могли выбирать их в центре приветствия.</span><span class="sxs-lookup"><span data-stu-id="26312-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="26312-134">Таким образом, из образа с несколькими языковыми пакетами программа установки отобразит список доступных языков и позволит пользователям выбрать один из них.</span><span class="sxs-lookup"><span data-stu-id="26312-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="26312-135">Затем все международные параметры устанавливаются в соответствии с выбранным языком или языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="26312-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="26312-136">Улучшенная модель обслуживания</span><span class="sxs-lookup"><span data-stu-id="26312-136">Improved servicing model</span></span>

<span data-ttu-id="26312-137">Один и тот же пакет QFE или исправления безопасности теперь можно установить поверх любых языковых систем.</span><span class="sxs-lookup"><span data-stu-id="26312-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="26312-138">Это очень важно, так как это позволяет быстрее исправлять исправления безопасности в частности и позволяет всем международным пользователям использовать те же возможности, что и все исправления безопасности.</span><span class="sxs-lookup"><span data-stu-id="26312-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="26312-139">Инфраструктура многоязыкового интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="26312-139">MUI infrastructure</span></span>

<span data-ttu-id="26312-140">Начиная с Windows Vista, доступны API многоязыкового интерфейса пользователя, позволяющие разработчикам воспользоваться преимуществами механизмов многоязыкового интерфейса пользователя для собственных приложений, не создавая пользовательскую логику для обработки ресурсов и управления языком.</span><span class="sxs-lookup"><span data-stu-id="26312-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="26312-141">Управление языками</span><span class="sxs-lookup"><span data-stu-id="26312-141">Language management</span></span>

<span data-ttu-id="26312-142">Базовые API MUI, которые предоставляют возможности управления языком интерфейса пользователя, доступны в составе инфраструктуры многоязыкового интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="26312-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="26312-143">Чтобы упростить управление различными параметрами языка пользовательского интерфейса на уровне системы, пользователя и приложения, MUI внутренне объединяет их в один список с приоритетом.</span><span class="sxs-lookup"><span data-stu-id="26312-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="26312-144">Затем MUI реализует резервный механизм на основе этого списка с приоритетом, позволяя выполнять частичные решения по локализации, одновременно предоставляя пользователям подходящий (если не рекомендуется) язык интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="26312-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="26312-145">Например, система, на которой работает Испанская версия Windows Vista с пакетом языкового интерфейса (LIP), установленная поверх базовой операционной системы, может поддерживать следующее поведение: сначала система попытается отображать свои ресурсы в каталанского, а если эти ресурсы недоступны в каталанского, вместо этого предоставьте пользователю доступ к испанским ресурсам.</span><span class="sxs-lookup"><span data-stu-id="26312-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="26312-146">Обработка ресурсов</span><span class="sxs-lookup"><span data-stu-id="26312-146">Resource handling</span></span>

<span data-ttu-id="26312-147">Благодаря улучшенной инфраструктуре многоязыкового интерфейса, доступной начиная с Windows Vista, наиболее распространенные технологии ресурсов поддерживают MUI.</span><span class="sxs-lookup"><span data-stu-id="26312-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="26312-148">В следующей таблице приведены дополнительные сведения о поддержке обработки ресурсов, доступной в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="26312-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26312-149">Категория</span><span class="sxs-lookup"><span data-stu-id="26312-149">Category</span></span></th>
<th><span data-ttu-id="26312-150">Поддержка</span><span class="sxs-lookup"><span data-stu-id="26312-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26312-151">Поддерживаемые типы ресурсов</span><span class="sxs-lookup"><span data-stu-id="26312-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="26312-152">Win32/неуправляемый ресурс:. DLL/. EXE/. OCX</span><span class="sxs-lookup"><span data-stu-id="26312-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="26312-153">Регистрации, связанные с оболочкой</span><span class="sxs-lookup"><span data-stu-id="26312-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="26312-154">Ресурсы, связанные с управлением: журнал событий, оснастка и MSC-файлы</span><span class="sxs-lookup"><span data-stu-id="26312-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="26312-155">WMI: MOF/МФЛ</span><span class="sxs-lookup"><span data-stu-id="26312-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="26312-156">Групповая политика: ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="26312-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="26312-157">Управляемый Resources.dll</span><span class="sxs-lookup"><span data-stu-id="26312-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26312-158">средства разработки:</span><span class="sxs-lookup"><span data-stu-id="26312-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="26312-159">Для Win32: RC.exe, MUIRCT.exe и Visual Studio 2005 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="26312-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26312-160">Поддержка ограниченного типа ресурсов</span><span class="sxs-lookup"><span data-stu-id="26312-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="26312-161">\*. chm, файлы справки</span><span class="sxs-lookup"><span data-stu-id="26312-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



