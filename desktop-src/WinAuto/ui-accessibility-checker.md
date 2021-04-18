---
title: Средства специальных возможностей — Аккчеккер (средство проверки доступности пользовательского интерфейса)
description: Описание Аккчеккер (средство проверки доступности пользовательского интерфейса), средства для тестирования модели автоматизации пользовательского интерфейса приложения или реализации Microsoft Active Accessibility (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- Средство UI Accessibility Checker
- аккчеккер
- Реализация модели автоматизации пользовательского интерфейса, тестирование
- Реализация UIA, тестирование
- Реализация Microsoft Active Accessibility, тестирование
- Реализация MSAA, тестирование
- тестирование автоматизации пользовательского интерфейса
- Тестирование UIA
- Тестирование Active Accessibility Майкрософт
- Тестирование MSAA
- Средства тестирования UIA
- Средства тестирования модели автоматизации пользовательского интерфейса
- Средства тестирования MSAA
- Средства тестирования Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "105700811"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="fdef0-117">Средства специальных возможностей — Аккчеккер (средство проверки доступности пользовательского интерфейса)</span><span class="sxs-lookup"><span data-stu-id="fdef0-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="fdef0-118">**Аккчеккер** (средство проверки доступности пользовательского интерфейса) проверяет соблюдение требований к специальным возможностям пользовательского интерфейса в проектировании и реализации модели автоматизации пользовательского интерфейса (UIA) или Microsoft Active ACCESSIBILITY (MSAA) независимо от базовой платформы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fdef0-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="fdef0-119">**Аккчеккер** также включает набор веб-проверок специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="fdef0-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="fdef0-120">**Аккчеккер** предоставляет следующие уровни функциональности:</span><span class="sxs-lookup"><span data-stu-id="fdef0-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="fdef0-121">Приложение графического пользовательского интерфейса Windows, которое поддерживает ручное тестирование, ведение журнала сообщений и создание подавления.</span><span class="sxs-lookup"><span data-stu-id="fdef0-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="fdef0-122">API для использования в платформах автоматического тестирования.</span><span class="sxs-lookup"><span data-stu-id="fdef0-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="fdef0-123">Консольное приложение, поддерживающее неуправляемую автоматизацию тестирования для сценариев, в которых нельзя использовать управляемый API **аккчеккер** .</span><span class="sxs-lookup"><span data-stu-id="fdef0-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="fdef0-124">Все уровни функциональных возможностей **аккчеккер** предоставляют подпрограммы для проверки программного доступа Microsoft Active Accessibility, создания программных событий, макета элементов управления и навигации с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="fdef0-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="fdef0-125">**Аккчеккер** также предоставляет базовую службу для записи в средство чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="fdef0-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="fdef0-126">**Аккчеккер** устанавливается вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="fdef0-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fdef0-127">Он находится в \\ папке bin \\ < *версии* > \\ < *Platform* > \\ аккчеккер пути установки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="fdef0-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="fdef0-128">**Аккчеккер** — это устаревшее средство.</span><span class="sxs-lookup"><span data-stu-id="fdef0-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="fdef0-129">Вместо этого рекомендуется использовать [аналитические сведения о специальных возможностях](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="fdef0-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdef0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="fdef0-130">Requirements</span></span>

<span data-ttu-id="fdef0-131">Требуется платформа .NET Framework 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fdef0-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="fdef0-132">**Аккчеккер** можно использовать для проверки специальных возможностей в системах без автоматизации пользовательского интерфейса Майкрософт, но только для анализа свойств Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="fdef0-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="fdef0-133">Для изучения автоматизации пользовательского интерфейса в системе должна присутствовать модель автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fdef0-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="fdef0-134">Дополнительные сведения см. в разделе "требования" [модели автоматизации пользовательского интерфейса](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="fdef0-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="fdef0-135">**Аккчеккер** устанавливается как часть общего набора средств в пакете Windows SDK, он не распространяется отдельно от отдельного файла для загрузки.</span><span class="sxs-lookup"><span data-stu-id="fdef0-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="fdef0-136">Windows SDK включает все средства, связанные со специальными возможностями, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="fdef0-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="fdef0-137">Получите Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fdef0-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="fdef0-138">(Кроме того, если требуется предыдущая версия, можно загрузить архив SDK, связанный с этой страницей.)</span><span class="sxs-lookup"><span data-stu-id="fdef0-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdef0-139">См. также</span><span class="sxs-lookup"><span data-stu-id="fdef0-139">Related topics</span></span>

- [<span data-ttu-id="fdef0-140">Средство Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="fdef0-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="fdef0-141">Проверить</span><span class="sxs-lookup"><span data-stu-id="fdef0-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="fdef0-142">Средства тестирования</span><span class="sxs-lookup"><span data-stu-id="fdef0-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="fdef0-143">Средство UI Automation Verify</span><span class="sxs-lookup"><span data-stu-id="fdef0-143">UI Automation Verify</span></span>](ui-automation-verify.md)
