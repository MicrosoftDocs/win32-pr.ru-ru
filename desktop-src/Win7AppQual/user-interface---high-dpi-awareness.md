---
description: 'Интерфейс пользователя: поддержка определения высоких значений DPI'
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Интерфейс пользователя: поддержка определения высоких значений DPI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116072"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="214e4-103">Интерфейс пользователя: поддержка определения высоких значений DPI</span><span class="sxs-lookup"><span data-stu-id="214e4-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="214e4-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="214e4-104">Affected Platforms</span></span>

 <span data-ttu-id="214e4-105">**Клиенты** — Windows XP Windows Vista, Windows \| \| 7</span><span class="sxs-lookup"><span data-stu-id="214e4-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="214e4-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="214e4-106">Feature Impact</span></span>

<span data-ttu-id="214e4-107">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="214e4-107">**Severity** - Medium</span></span>  
<span data-ttu-id="214e4-108">**Частота** — средний</span><span class="sxs-lookup"><span data-stu-id="214e4-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="214e4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="214e4-109">Description</span></span>

<span data-ttu-id="214e4-110">Задача заключается в том, чтобы обеспечить конечным пользователям возможность устанавливать свои дисплеи в собственном разрешении и использовать DPI, а не разрешение экрана, чтобы изменить размер отображаемого текста и изображений.</span><span class="sxs-lookup"><span data-stu-id="214e4-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="214e4-111">Windows 7 может автоматически обнаруживать и настраивать DPI по умолчанию для чистых установок на компьютерах, настроенных изготовителями оборудования, с помощью параметров DPI.</span><span class="sxs-lookup"><span data-stu-id="214e4-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="214e4-112">Существуют инструменты, которые можно использовать для разработки приложений с высоким DPI, чтобы обеспечить наиболее удобочитаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="214e4-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="214e4-113">Мы добавили две новые функции высокого DPI в Windows 7:</span><span class="sxs-lookup"><span data-stu-id="214e4-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="214e4-114">Параметр DPI для каждого пользователя (ранее на компьютере)</span><span class="sxs-lookup"><span data-stu-id="214e4-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="214e4-115">Изменение DPI без перезагрузки (по-прежнему требуется выход из системы и вход в систему)</span><span class="sxs-lookup"><span data-stu-id="214e4-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="214e4-116">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="214e4-116">Manifestation of Impact</span></span>

<span data-ttu-id="214e4-117">Приложения, которые не обрабатывают регистр с высоким разрешением, скорее всего, демонстрируют визуальные артефакты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="214e4-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="214e4-118">Обрезка пользовательского интерфейса или текста другими элементами пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="214e4-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="214e4-119">Непоследовательные размеры шрифтов</span><span class="sxs-lookup"><span data-stu-id="214e4-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="214e4-120">Пользовательский интерфейс для экрана</span><span class="sxs-lookup"><span data-stu-id="214e4-120">Off-screen UIs</span></span>
-   <span data-ttu-id="214e4-121">Размытие текста или пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="214e4-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="214e4-122">Нарушено перетаскивание или другие входные данные</span><span class="sxs-lookup"><span data-stu-id="214e4-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="214e4-123">Отображение полноэкранных приложений DX частично из экрана</span><span class="sxs-lookup"><span data-stu-id="214e4-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="214e4-124">Решение</span><span class="sxs-lookup"><span data-stu-id="214e4-124">Solution</span></span>

<span data-ttu-id="214e4-125">Чтобы сделать приложения совместимыми с DPI:</span><span class="sxs-lookup"><span data-stu-id="214e4-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="214e4-126">Выполните высокоуровневый функциональный этап тестирования, включая установку и удаление со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="214e4-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="214e4-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="214e4-127">Setting</span></span>                                              | <span data-ttu-id="214e4-128">Что искать</span><span class="sxs-lookup"><span data-stu-id="214e4-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="214e4-129">1024x768 @ 120 DPI (125% масштабирования)</span><span class="sxs-lookup"><span data-stu-id="214e4-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="214e4-130">Это эффективное разрешение, равное ~ 800x600, поэтому Поиск пользовательского интерфейса, вырезая с экрана или с разметкой, не вызывает проблем.</span><span class="sxs-lookup"><span data-stu-id="214e4-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="214e4-131">Также найдите точечные рисунки пиксилатед & значков.</span><span class="sxs-lookup"><span data-stu-id="214e4-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="214e4-132">1600x1200 @144 dpi (150% масштабирования)</span><span class="sxs-lookup"><span data-stu-id="214e4-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="214e4-133">Нечеткий пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="214e4-133">Blurry UI.</span></span> <span data-ttu-id="214e4-134">Убедитесь, что все операции с мышью работают, особенно перетащите & операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="214e4-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="214e4-135">Также убедитесь, что полноэкранный режим работает правильно.</span><span class="sxs-lookup"><span data-stu-id="214e4-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="214e4-136">1600x1200 @ 144 DPI с отключенной виртуализацией DPI</span><span class="sxs-lookup"><span data-stu-id="214e4-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="214e4-137">Часто кнопки и пользовательский интерфейс не масштабируются по отношению к более крупному тексту & будет заметно обрезать текст.</span><span class="sxs-lookup"><span data-stu-id="214e4-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="214e4-138">Найдите проблемы макета в общих & пиксилатед битматс значки &.</span><span class="sxs-lookup"><span data-stu-id="214e4-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="214e4-139">Запишите все найденные проблемы, включая расположение, разрешение экрана и параметры DPI, а также сведения о том, как приложение работает в других конфигурациях DPI и разрешения для полноты.</span><span class="sxs-lookup"><span data-stu-id="214e4-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="214e4-140">Проверьте каждую из проблем, связанных с кодом общего количества точек на дюйм</span><span class="sxs-lookup"><span data-stu-id="214e4-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="214e4-141">Оцените стоимость выполнения полного DPI в приложении</span><span class="sxs-lookup"><span data-stu-id="214e4-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="214e4-142">Создание списка ресурсов с высоким DPI (например, кнопок, значков)</span><span class="sxs-lookup"><span data-stu-id="214e4-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="214e4-143">Обработайте и исправьте список проблем DPI, найденных на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="214e4-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="214e4-144">Интегрируйте новые ресурсы из шага 5</span><span class="sxs-lookup"><span data-stu-id="214e4-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="214e4-145">Объявление приложения на уровне DPI</span><span class="sxs-lookup"><span data-stu-id="214e4-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="214e4-146">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="214e4-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="214e4-147">Повторно запустите оценку соответствия DPI и убедитесь, что проблемы устранены.</span><span class="sxs-lookup"><span data-stu-id="214e4-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="214e4-148">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="214e4-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="214e4-149">Разработка приложений с высоким разрешением для настольных систем в Windows</span><span class="sxs-lookup"><span data-stu-id="214e4-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="214e4-150">**Вопросы и ответы по техническим вопросам:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="214e4-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
