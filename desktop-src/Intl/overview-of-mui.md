---
description: В этом разделе приводятся общие сведения о технологии многоязыкового пользовательского интерфейса (MUI), поддержке платформ, предоставляемой для многоязыкового взаимодействия с пользователем, и преимуществах, предоставляемых ИТ-экосистеме Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Обзор MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563465"
---
# <a name="overview-of-mui"></a><span data-ttu-id="d4d60-103">Обзор MUI</span><span class="sxs-lookup"><span data-stu-id="d4d60-103">Overview of MUI</span></span>

<span data-ttu-id="d4d60-104">В этом разделе приводятся общие сведения о технологии многоязыкового пользовательского интерфейса (MUI), поддержке платформ, предоставляемой для многоязыкового взаимодействия с пользователем, и преимуществах, предоставляемых ИТ-экосистеме Windows.</span><span class="sxs-lookup"><span data-stu-id="d4d60-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="d4d60-105">На этой странице:</span><span class="sxs-lookup"><span data-stu-id="d4d60-105">On this page:</span></span>

-   [<span data-ttu-id="d4d60-106">Потребность в многоязычных вычислениях</span><span class="sxs-lookup"><span data-stu-id="d4d60-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="d4d60-107">Роль многоязыкового интерфейса пользователя при включении многоязычных вычислений</span><span class="sxs-lookup"><span data-stu-id="d4d60-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="d4d60-108">Основные понятия MUI</span><span class="sxs-lookup"><span data-stu-id="d4d60-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="d4d60-109">Журнал многоязыкового интерфейса пользователя в Windows</span><span class="sxs-lookup"><span data-stu-id="d4d60-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="d4d60-110">Преимущества технологии MUI</span><span class="sxs-lookup"><span data-stu-id="d4d60-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="d4d60-111">Потребность в многоязычных вычислениях</span><span class="sxs-lookup"><span data-stu-id="d4d60-111">The need for multilingual computing</span></span>

<span data-ttu-id="d4d60-112">Чтобы получить преимущества от возможностей роста, представленных международными рынками, платформы и приложения Майкрософт поддерживают больше языков, культур и рынков, чем когда-либо ранее.</span><span class="sxs-lookup"><span data-stu-id="d4d60-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="d4d60-113">Язык, язык и региональные параметры и особенности рынка по-прежнему важны для международных пользователей, несмотря на повышение тенденций глобализации.</span><span class="sxs-lookup"><span data-stu-id="d4d60-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="d4d60-114">На следующей круговой диаграмме показано, что динамики, отличные от английского, по-прежнему составляют 91,5 процентов населения мира.</span><span class="sxs-lookup"><span data-stu-id="d4d60-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![Круговая диаграмма с тремя сегментами; один из них с меткой "неанглийские динамики 91,5%" значительно больше, чем два других Объединенных](images/overview-of-mui-fig1.gif)

<span data-ttu-id="d4d60-116">Во всем мире есть 193 стран и более 6 900 известных языков, используемых сегодня.</span><span class="sxs-lookup"><span data-stu-id="d4d60-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="d4d60-117">На английском языке, несмотря на его роль в качестве бизнес-языка мира, говорят только 8,5% населения мира в качестве первого или второго языка.</span><span class="sxs-lookup"><span data-stu-id="d4d60-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="d4d60-118">Чтобы предоставить собственную информацию 94% населения мира, эти сведения должны быть доступны в 347 (около 5%). мировых языков, имеющих по крайней мере миллион докладчиков.</span><span class="sxs-lookup"><span data-stu-id="d4d60-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="d4d60-119">Это особенно важно, так как тренды глобализации увеличивают ожидания этих пользователей в отношении технологий и их доступности на своих рынках.</span><span class="sxs-lookup"><span data-stu-id="d4d60-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="d4d60-120">Необходимость локализовать программное обеспечение на других языках увеличилась в течение многих лет, и корпорация Майкрософт теперь предоставляет Windows Vista и другие продукты на большем числе языков, чем когда-либо.</span><span class="sxs-lookup"><span data-stu-id="d4d60-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="d4d60-121">Эта эволюция особенно понятна в Microsoft Windows, так как она прекратила поддержку 30 языков с Windows 98 и почти 100 с Windows Vista, как показано на следующей линейчатой диаграмме.</span><span class="sxs-lookup"><span data-stu-id="d4d60-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![Линейчатая диаграмма, показывающая, что количество языков в Windows Vista гораздо больше, чем в Windows 98 или Windows XP](images/overview-of-mui-fig2.gif)

<span data-ttu-id="d4d60-123">*Рис. 2. число языков, поддерживаемых выпусками Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="d4d60-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="d4d60-124">Роль многоязыкового интерфейса пользователя при включении многоязычных вычислений</span><span class="sxs-lookup"><span data-stu-id="d4d60-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="d4d60-125">Как обсуждалось в предыдущем разделе, [глобализация](glossary-for-understanding-mui.md) и [Локализация](glossary-for-understanding-mui.md) приложений стали в более глобально интегрированном мире.</span><span class="sxs-lookup"><span data-stu-id="d4d60-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="d4d60-126">В частности, так как все большее и большее число предприятий становится глобальным, внутренним или через их бизнес-сети, потребность в многоязычных приложениях значительно возрастает.</span><span class="sxs-lookup"><span data-stu-id="d4d60-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="d4d60-127">Так что в настоящее время эти компании сталкиваются с разворачиванием этих приложений глобально.</span><span class="sxs-lookup"><span data-stu-id="d4d60-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="d4d60-128">Поддержка дополнительных языков для операционных систем Windows, а также программных приложений, созданных для платформы Windows, требует новых стратегий, позволяющих реализовать все основные сценарии с минимальными затратами на проектирование.</span><span class="sxs-lookup"><span data-stu-id="d4d60-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="d4d60-129">Технология многоязыкового интерфейса пользователя предназначена для разработчиков и независимых поставщиков программного обеспечения, надежде создавать и поддерживать многоязычные приложения для платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="d4d60-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="d4d60-130">MUI также имеет ключевое значение для изготовителей оборудования и предприятий, которые могут использовать его для развертывания операционной системы Windows и добавления приложений на компьютеры разных языков с помощью развертывания одного образа.</span><span class="sxs-lookup"><span data-stu-id="d4d60-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="d4d60-131">Основные понятия MUI</span><span class="sxs-lookup"><span data-stu-id="d4d60-131">Core concepts of MUI</span></span>

<span data-ttu-id="d4d60-132">Основная идея многоязыкового интерфейса пользователя заключается в том, чтобы [отделить хранилище локализуемых ресурсов от исходного кода приложения](mui-fundamental-concepts-explained.md), чтобы иметь возможность спроектировать любое многоязыкическое приложение как сочетание двоичного файла, не зависящего от языка, и набора локализованных файлов ресурсов, зависящих от языка.</span><span class="sxs-lookup"><span data-stu-id="d4d60-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="d4d60-133">После сохранения исходного кода приложения отдельно от локализованных ресурсов становится нелегко [динамически загружать соответствующие локализованные ресурсы](mui-fundamental-concepts-explained.md) для контекста приложения на основе логики, которая учитывает параметры системы, пользователя и уровня приложения для языка пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d4d60-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="d4d60-134">Эти фундаментальные атрибуты MUI помогают упростить бизнес-сценарии, например:</span><span class="sxs-lookup"><span data-stu-id="d4d60-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="d4d60-135">Улучшенная модель локализации для пользовательского интерфейса и содержимого справки с помощью физического разделения исходного кода приложения и локализуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4d60-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="d4d60-136">Рассматривая локализуемые ресурсы как динамическое содержимое и загружая их в соответствии с настройками языка пользовательского интерфейса и резервными параметрами.</span><span class="sxs-lookup"><span data-stu-id="d4d60-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="d4d60-137">Это позволяет выполнять такие сценарии, как:</span><span class="sxs-lookup"><span data-stu-id="d4d60-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="d4d60-138">Переключение с одного языка пользовательского интерфейса на другой во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4d60-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="d4d60-139">Создание региональных или международных образов с единым развертыванием, охватывающим набор языков для изготовителей оборудования и организаций.</span><span class="sxs-lookup"><span data-stu-id="d4d60-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="d4d60-140">Журнал многоязыкового интерфейса пользователя в Windows</span><span class="sxs-lookup"><span data-stu-id="d4d60-140">History of MUI in Windows</span></span>

<span data-ttu-id="d4d60-141">Уровень поддержки, доступный для многоязыкового взаимодействия с пользователем на уровне операционной системы Windows и для разработки многоязычных приложений на платформе Windows, развивается со временем и по различным версиям Windows.</span><span class="sxs-lookup"><span data-stu-id="d4d60-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="d4d60-142">Поддерживаемые функции [до Windows Vista](evolution-of-mui-support-across-windows-versions.md) были достаточно базовыми, с одноязыковыми образами Windows и возможностью добавления пакетов многоязычного пользовательского интерфейса в определенные сценарии.</span><span class="sxs-lookup"><span data-stu-id="d4d60-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="d4d60-143">Не была доступна поддержка разработчиков многоязычных приложений.</span><span class="sxs-lookup"><span data-stu-id="d4d60-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="d4d60-144">В [Windows Vista](evolution-of-mui-support-across-windows-versions.md)Корпорация Майкрософт внесла значительные инвестиции в MUI, и Windows Vista построена с нуля на платформе MUI.</span><span class="sxs-lookup"><span data-stu-id="d4d60-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="d4d60-145">Хотя это и является основной стратегией в стратегии локализации Windows, так как она является ключевым средством, которое позволяет корпорации Майкрософт предоставлять Windows на более языках, чем когда-либо ранее, оно является первым и главным для пользователей Windows, разработчиков и клиентов.</span><span class="sxs-lookup"><span data-stu-id="d4d60-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="d4d60-146">Он предоставляет следующие основные преимущества:</span><span class="sxs-lookup"><span data-stu-id="d4d60-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="d4d60-147">Не зависящая от языка операционная система со встроенной поддержкой многоязыкового интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4d60-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="d4d60-148">Настраиваемая упаковка, развертывание и установка для поддержки многоязычных сценариев.</span><span class="sxs-lookup"><span data-stu-id="d4d60-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="d4d60-149">Развертывание с одним образом с несколькими языками.</span><span class="sxs-lookup"><span data-stu-id="d4d60-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="d4d60-150">Улучшенная модель обслуживания, в которой исполняемый код может обновляться независимо от ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4d60-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="d4d60-151">Поддержка разработчиков для создания многоязычных приложений.</span><span class="sxs-lookup"><span data-stu-id="d4d60-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="d4d60-152">В следующей таблице представлен подробный обзор поддержки платформы Windows для многоязыкового интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4d60-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4d60-153">Категория</span><span class="sxs-lookup"><span data-stu-id="d4d60-153">Category</span></span></th>
<th><span data-ttu-id="d4d60-154">Поддержка</span><span class="sxs-lookup"><span data-stu-id="d4d60-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4d60-155">Поддерживаемые версии Windows (только поддержка ОС)</span><span class="sxs-lookup"><span data-stu-id="d4d60-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4d60-156">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4d60-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="d4d60-157">Семейство серверов Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d4d60-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="d4d60-158">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="d4d60-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="d4d60-159">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="d4d60-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="d4d60-160">Семейство Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4d60-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="d4d60-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="d4d60-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4d60-162">Поддерживаемые версии Windows (поддержка приложений & ОС)</span><span class="sxs-lookup"><span data-stu-id="d4d60-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4d60-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4d60-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4d60-164">Неподдерживаемые версии Windows</span><span class="sxs-lookup"><span data-stu-id="d4d60-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="d4d60-165">Windows 9x</span><span class="sxs-lookup"><span data-stu-id="d4d60-165">Windows 9x</span></span></li>
<li><span data-ttu-id="d4d60-166">Windows Me</span><span class="sxs-lookup"><span data-stu-id="d4d60-166">Windows Me</span></span></li>
<li><span data-ttu-id="d4d60-167">Windows XP Home Edition</span><span class="sxs-lookup"><span data-stu-id="d4d60-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="d4d60-168">Преимущества технологии MUI</span><span class="sxs-lookup"><span data-stu-id="d4d60-168">Benefits of MUI technology</span></span>

<span data-ttu-id="d4d60-169">MUI позитивно влияет на несколько аспектов экосистемы Windows:</span><span class="sxs-lookup"><span data-stu-id="d4d60-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="d4d60-170">[Преимущества для разработчиков](benefits-of-mui-explained.md). многочисленные преимущества предоставляются разработчикам приложений с помощью поддержки API MUI для создания многоязычных приложений, смоделированных на основе тех же принципов, что и многоязычная поддержка в самой основной операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="d4d60-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="d4d60-171">К этим преимуществам относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="d4d60-171">These benefits include:</span></span>
    -   <span data-ttu-id="d4d60-172">Возможность предоставить язык интерфейса, который соответствует самой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="d4d60-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="d4d60-173">Возможность легко расширить языковую поддержку приложения.</span><span class="sxs-lookup"><span data-stu-id="d4d60-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="d4d60-174">Возможность легко обслуживать и обслуживать приложение.</span><span class="sxs-lookup"><span data-stu-id="d4d60-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="d4d60-175">Возможность включения развертывания приложений с одним образом с помощью поставщиков вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="d4d60-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="d4d60-176">[Преимущества для предприятий](benefits-of-mui-explained.md). основное преимущество многоязыкового интерфейса пользователя для предприятий — возможность развертывания, поддержки и поддержания одинакового многоязыкового образа в рамках одной установки.</span><span class="sxs-lookup"><span data-stu-id="d4d60-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="d4d60-177">Еще одна значительная выигрыш заключается в поддержке многоязычных настольных систем, которые обеспечивают эффективное взаимодействие с пользователями с использованием различных языковых настроек.</span><span class="sxs-lookup"><span data-stu-id="d4d60-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="d4d60-178">[Преимущества для изготовителей оборудования](benefits-of-mui-explained.md). Основным преимуществом для изготовителей оборудования является установка единого образа, которую обеспечивает MUI, с поддержкой нескольких языков, что обеспечивает более эффективное управление инвентаризацией.</span><span class="sxs-lookup"><span data-stu-id="d4d60-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="d4d60-179">Изготовители оборудования также получают преимущества поддержки многоязыкового интерфейса пользователя для разработки приложений, так как позволяют им добавлять приложения на свои образы, одновременно используя преимущества установки одного образа, если эти приложения поддерживают MUI.</span><span class="sxs-lookup"><span data-stu-id="d4d60-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 




