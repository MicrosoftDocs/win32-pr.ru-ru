---
title: Проверочные тесты для встроенных Интернет-магазинов типа 2
description: В этом разделе описываются тесты, которые Майкрософт будет выполнять для проверки Интернет-магазина типа 2. Корпорация Майкрософт требует, чтобы эти тесты выполнялись перед отправкой версии-кандидата. Ваш Интернет-магазин должен успешно передавать эти тесты для публикации.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Интернет-магазины проигрывателя Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411001"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="4c616-106">Проверочные тесты для встроенных Интернет-магазинов типа 2</span><span class="sxs-lookup"><span data-stu-id="4c616-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="4c616-107">В этом разделе описываются тесты, которые Майкрософт будет выполнять для проверки Интернет-магазина типа 2.</span><span class="sxs-lookup"><span data-stu-id="4c616-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="4c616-108">Корпорация Майкрософт требует, чтобы эти тесты выполнялись перед отправкой версии-кандидата.</span><span class="sxs-lookup"><span data-stu-id="4c616-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="4c616-109">Ваш Интернет-магазин должен успешно передавать эти тесты для публикации.</span><span class="sxs-lookup"><span data-stu-id="4c616-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="4c616-110">Если магазин имеет тип 1, а не тип 2, этот раздел можно использовать в качестве рекомендации для понимания области тестирования сертификации, которая рассматривается для магазинов типа 1.</span><span class="sxs-lookup"><span data-stu-id="4c616-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="4c616-111">Чтобы получить полный набор тестов для магазинов типа 1, обратитесь в [Служба поддержки Майкрософт](https://support.microsoft.com/ph/7763#tab0).</span><span class="sxs-lookup"><span data-stu-id="4c616-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="4c616-112">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="4c616-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4c616-113">Контрольный список теста</span><span class="sxs-lookup"><span data-stu-id="4c616-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="4c616-114">Подготовка тестового прохода</span><span class="sxs-lookup"><span data-stu-id="4c616-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="4c616-115">Тестовая среда</span><span class="sxs-lookup"><span data-stu-id="4c616-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="4c616-116">Настройка и установка</span><span class="sxs-lookup"><span data-stu-id="4c616-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="4c616-117">Настройка тестового компьютера</span><span class="sxs-lookup"><span data-stu-id="4c616-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="4c616-118">Настройка магазина</span><span class="sxs-lookup"><span data-stu-id="4c616-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="4c616-119">Создание учетной записи</span><span class="sxs-lookup"><span data-stu-id="4c616-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="4c616-120">Настройка кэширования учетных данных</span><span class="sxs-lookup"><span data-stu-id="4c616-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="4c616-121">Получение содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="4c616-122">Потоковая передача содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="4c616-123">Получение содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="4c616-124">Запись содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="4c616-125">Передача содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="4c616-126">Функции магазина</span><span class="sxs-lookup"><span data-stu-id="4c616-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="4c616-127">Управление учетной записью</span><span class="sxs-lookup"><span data-stu-id="4c616-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="4c616-128">Управление информационным центром</span><span class="sxs-lookup"><span data-stu-id="4c616-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="4c616-129">Взаимодействие с магазином</span><span class="sxs-lookup"><span data-stu-id="4c616-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="4c616-130">Возврат в активное хранилище</span><span class="sxs-lookup"><span data-stu-id="4c616-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="4c616-131">Предотвращение того, что проверенное хранилище будет переделаться через активное хранилище</span><span class="sxs-lookup"><span data-stu-id="4c616-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="4c616-132">Доступ к хранилищу в режиме High-Contrast</span><span class="sxs-lookup"><span data-stu-id="4c616-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="4c616-133">Защита хранилища</span><span class="sxs-lookup"><span data-stu-id="4c616-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="4c616-134">Контрольный список теста</span><span class="sxs-lookup"><span data-stu-id="4c616-134">Test Checklist</span></span>

<span data-ttu-id="4c616-135">Используйте контрольный список, приведенный в следующей таблице, чтобы проверить Интернет-магазин типа 2, который вы хотите подключить к доске.</span><span class="sxs-lookup"><span data-stu-id="4c616-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="4c616-136">Тест</span><span class="sxs-lookup"><span data-stu-id="4c616-136">Test</span></span>

<span data-ttu-id="4c616-137">Windows XP;</span><span class="sxs-lookup"><span data-stu-id="4c616-137">Windows XP</span></span>

<span data-ttu-id="4c616-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c616-138">Windows Vista</span></span>

<span data-ttu-id="4c616-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c616-139">Windows 7</span></span>

<span data-ttu-id="4c616-140">Результат (пройденный/недопустимый/неприменимый)</span><span class="sxs-lookup"><span data-stu-id="4c616-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="4c616-141">32</span><span class="sxs-lookup"><span data-stu-id="4c616-141">32</span></span>

<span data-ttu-id="4c616-142">64</span><span class="sxs-lookup"><span data-stu-id="4c616-142">64</span></span>

<span data-ttu-id="4c616-143">32</span><span class="sxs-lookup"><span data-stu-id="4c616-143">32</span></span>

<span data-ttu-id="4c616-144">64</span><span class="sxs-lookup"><span data-stu-id="4c616-144">64</span></span>

<span data-ttu-id="4c616-145">32</span><span class="sxs-lookup"><span data-stu-id="4c616-145">32</span></span>

<span data-ttu-id="4c616-146">64</span><span class="sxs-lookup"><span data-stu-id="4c616-146">64</span></span>

1. <span data-ttu-id="4c616-147">Убедитесь, что установка программного обеспечения выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c616-147">Verify that software installs.</span></span>

2. <span data-ttu-id="4c616-148">Убедитесь, что программное обеспечение удаляется.</span><span class="sxs-lookup"><span data-stu-id="4c616-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="4c616-149">Убедитесь, что программное обеспечение не выполняется в области.</span><span class="sxs-lookup"><span data-stu-id="4c616-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="4c616-150">Убедитесь, что вкладка хранилище работает.</span><span class="sxs-lookup"><span data-stu-id="4c616-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="4c616-151">Убедитесь, что в хранилище есть возможность создать новую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4c616-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="4c616-152">Убедитесь, что созданная учетная запись может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="4c616-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="4c616-153">Убедитесь, что в хранилище есть возможность сохранить сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="4c616-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="4c616-154">Убедитесь, что кэширование учетных данных имеется и работает.</span><span class="sxs-lookup"><span data-stu-id="4c616-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="4c616-155">Убедитесь, что пользователю предлагается ввести учетные данные, если они не кэшированы.</span><span class="sxs-lookup"><span data-stu-id="4c616-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="4c616-156">Убедитесь, что все доступные типы потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c616-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="4c616-157">Убедитесь, что содержимое воспроизводится в проигрывателе Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4c616-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="4c616-158">Убедитесь, что вычисленная цена правильная.</span><span class="sxs-lookup"><span data-stu-id="4c616-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="4c616-159">Убедитесь, что приобретенное содержимое загружено в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="4c616-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="4c616-160">Убедитесь, что метаданные скачаны для покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="4c616-161">Убедитесь, что права на использование мультимедиа указаны правильно для покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="4c616-162">Убедитесь, что приобретенное содержимое можно воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="4c616-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="4c616-163">Убедитесь, что кнопка **купить** или **магазин** будет переключена в магазин.</span><span class="sxs-lookup"><span data-stu-id="4c616-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="4c616-164">Убедитесь, что приобретенное содержимое загружено.</span><span class="sxs-lookup"><span data-stu-id="4c616-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="4c616-165">Убедитесь, что приобретенное содержимое можно записать.</span><span class="sxs-lookup"><span data-stu-id="4c616-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="4c616-166">Убедитесь, что счетчик записи уменьшен.</span><span class="sxs-lookup"><span data-stu-id="4c616-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="4c616-167">Убедитесь, что содержимое можно передать на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="4c616-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="4c616-168">Убедитесь, что содержимое передается на устройство.</span><span class="sxs-lookup"><span data-stu-id="4c616-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="4c616-169">Убедитесь, что счетчик синхронизации уменьшен.</span><span class="sxs-lookup"><span data-stu-id="4c616-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="4c616-170">Убедитесь, что История приобретений отслеживает предыдущие покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="4c616-171">Убедитесь, что возможно восстановление предыдущей покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="4c616-172">Проверка функциональных возможностей магазина для управления несколькими компьютерами.</span><span class="sxs-lookup"><span data-stu-id="4c616-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="4c616-173">Убедитесь, что центр информации по умолчанию отключен.</span><span class="sxs-lookup"><span data-stu-id="4c616-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="4c616-174">Убедитесь, что информационный центр содержит сведения о файлах мультимедиа в области немедленного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4c616-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="4c616-175">Убедитесь, что ссылки переходят в хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c616-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="4c616-176">Убедитесь, что проверенное хранилище выдает активное хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c616-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="4c616-177">Убедитесь, что проверенное хранилище не занимает текущее хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c616-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="4c616-178">Убедитесь, что хранилище доступно в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="4c616-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="4c616-179">Убедитесь, что хранилище защищено.</span><span class="sxs-lookup"><span data-stu-id="4c616-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="4c616-180">Подготовка тестового прохода</span><span class="sxs-lookup"><span data-stu-id="4c616-180">Test Pass Preparation</span></span>

<span data-ttu-id="4c616-181">Прежде чем запустить тестовый проход, убедитесь, что хранилище и тестовые учетные записи готовы к тестированию.</span><span class="sxs-lookup"><span data-stu-id="4c616-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="4c616-182">Перед началом передачи необходимо определить следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="4c616-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="4c616-183">Если вы можете определить сведения за несколько дней до тестового прохода, этот проход будет выполняться более эффективно.</span><span class="sxs-lookup"><span data-stu-id="4c616-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="4c616-184">Определите следующие сведения о тестовых учетных записях, предоставляемых магазином:</span><span class="sxs-lookup"><span data-stu-id="4c616-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="4c616-185">Учетные записи и пароли позволяют пользователю входить</span><span class="sxs-lookup"><span data-stu-id="4c616-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="4c616-186">Учетные записи правильно и имеют достаточный фонд для каждого типа бизнес-режима, предлагаемого магазином</span><span class="sxs-lookup"><span data-stu-id="4c616-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="4c616-187">Учетные записи действительны для всех локальных языков, или учетные записи существуют для каждого языкового стандарта, если учетные записи не могут пересекать язык.</span><span class="sxs-lookup"><span data-stu-id="4c616-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="4c616-188">Определите, какие языковые стандарты следует проверить.</span><span class="sxs-lookup"><span data-stu-id="4c616-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="4c616-189">Определите, какие языки следует тестировать.</span><span class="sxs-lookup"><span data-stu-id="4c616-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="4c616-190">Определите следующие сведения о тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="4c616-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="4c616-191">Динамические магазины, работающие с Windows XP, Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c616-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="4c616-192">Неактивное хранилище для тестирования</span><span class="sxs-lookup"><span data-stu-id="4c616-192">The non-live store to test</span></span>
    -   <span data-ttu-id="4c616-193">Убедитесь, что неактивное хранилище для проверки отображается во всех версиях операционной системы и на всех версиях платформы проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="4c616-194">Определите следующие сведения о магазине для тестирования:</span><span class="sxs-lookup"><span data-stu-id="4c616-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="4c616-195">Имя хранилища</span><span class="sxs-lookup"><span data-stu-id="4c616-195">Store name</span></span>
    -   <span data-ttu-id="4c616-196">Ожидаемая графика и метка для логотипа на вкладке Store</span><span class="sxs-lookup"><span data-stu-id="4c616-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="4c616-197">Является ли хранилище активным для всех версий операционной системы?</span><span class="sxs-lookup"><span data-stu-id="4c616-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="4c616-198">Это новая версия тестируемого хранилища?</span><span class="sxs-lookup"><span data-stu-id="4c616-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="4c616-199">Хранится ли хранилище в тесте типа 1 или 2?</span><span class="sxs-lookup"><span data-stu-id="4c616-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="4c616-200">Изменился ли тип хранилища?</span><span class="sxs-lookup"><span data-stu-id="4c616-200">Has the store type changed?</span></span>

-   <span data-ttu-id="4c616-201">Определите версии операционной системы и платформы, которые планируется протестировать магазин.</span><span class="sxs-lookup"><span data-stu-id="4c616-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="4c616-202">Убедитесь, что установщик и подключаемый модуль работают во всех версиях операционных систем и на тестируемых платформах.</span><span class="sxs-lookup"><span data-stu-id="4c616-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="4c616-203">Определите, требуется ли документ навигации.</span><span class="sxs-lookup"><span data-stu-id="4c616-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="4c616-204">Определите следующие сведения о носителе, предлагаемом магазином.</span><span class="sxs-lookup"><span data-stu-id="4c616-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="4c616-205">Форматы</span><span class="sxs-lookup"><span data-stu-id="4c616-205">Formats</span></span>
    -   <span data-ttu-id="4c616-206">Требуется ли собственное программное обеспечение?</span><span class="sxs-lookup"><span data-stu-id="4c616-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="4c616-207">Нужно ли протестировать все типы носителей или только подмножество типов мультимедиа?</span><span class="sxs-lookup"><span data-stu-id="4c616-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="4c616-208">Определите следующие сведения о правах на использование мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="4c616-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="4c616-209">Имеет ли носитель для хранения защиту содержимого?</span><span class="sxs-lookup"><span data-stu-id="4c616-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="4c616-210">Если это так, определите тип защиты содержимого, имеющийся на носителе.</span><span class="sxs-lookup"><span data-stu-id="4c616-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="4c616-211">Если это так, определите ожидаемое защищенное поведение.</span><span class="sxs-lookup"><span data-stu-id="4c616-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="4c616-212">Есть ли права на использование мультимедиа для общего доступа между компьютерами?</span><span class="sxs-lookup"><span data-stu-id="4c616-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="4c616-213">Права на синхронизацию</span><span class="sxs-lookup"><span data-stu-id="4c616-213">The sync rights</span></span>
    -   <span data-ttu-id="4c616-214">Права на запись</span><span class="sxs-lookup"><span data-stu-id="4c616-214">The burn rights</span></span>
    -   <span data-ttu-id="4c616-215">Права на воспроизведение</span><span class="sxs-lookup"><span data-stu-id="4c616-215">The play rights</span></span>
    -   <span data-ttu-id="4c616-216">Даты истечения срока действия, если таковые имеются</span><span class="sxs-lookup"><span data-stu-id="4c616-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="4c616-217">Определите, достаточно ли носителей (достаточно большого каталога), чтобы предоставить осмысленный пример.</span><span class="sxs-lookup"><span data-stu-id="4c616-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="4c616-218">Определите, что проходит этап: RC 0, соответствие и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c616-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="4c616-219">Определить, является ли тестовый проход определенным типом: регрессия, тестового состояния и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c616-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="4c616-220">Тестовая среда</span><span class="sxs-lookup"><span data-stu-id="4c616-220">Test Environment</span></span>

<span data-ttu-id="4c616-221">Необходимо провести тестирование в следующих конфигурациях:</span><span class="sxs-lookup"><span data-stu-id="4c616-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="4c616-222">Microsoft Windows Media Player 11 в Windows XP с пакетом обновления 3 (SP3) 32-разрядные и 64-разрядные операционные системы</span><span class="sxs-lookup"><span data-stu-id="4c616-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="4c616-223">Windows Media Player 11 в Windows Vista с 32-разрядными и 64-разрядными системами (32-разрядный проигрыватель Windows Media)</span><span class="sxs-lookup"><span data-stu-id="4c616-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="4c616-224">Проигрыватель Microsoft Windows Media Player 12 в Windows 7 32-разрядных и 64-разрядных операционных системах (32-разрядный проигрыватель Windows Media)</span><span class="sxs-lookup"><span data-stu-id="4c616-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="4c616-225">Несмотря на то, что необходимо выполнить тестирование на всех указанных версиях операционной системы и платформах, 32-разрядные версии Windows Vista и Windows 7 являются приоритетными целевыми версиями операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c616-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="4c616-226">Необходимо протестировать установку любого программного обеспечения на всех платформах.</span><span class="sxs-lookup"><span data-stu-id="4c616-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="4c616-227">Снимки экрана в этом разделе используют вымышленное хранилище Proseware, чтобы продемонстрировать использование пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4c616-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="4c616-228">Настройка и установка</span><span class="sxs-lookup"><span data-stu-id="4c616-228">Configuration and Setup</span></span>

<span data-ttu-id="4c616-229">В следующих разделах описывается настройка и настройка проверочного тестирования для интерактивного магазина типа 2.</span><span class="sxs-lookup"><span data-stu-id="4c616-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="4c616-230">Настройка тестового компьютера</span><span class="sxs-lookup"><span data-stu-id="4c616-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="4c616-231">Чтобы настроить тестовый компьютер, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4c616-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="4c616-232">Наведите тестовый компьютер на тестовые серверы содержимого, добавив раздел реестра, относящийся к конкретному магазину.</span><span class="sxs-lookup"><span data-stu-id="4c616-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="4c616-233">Задайте нужные параметры языка и языкового стандарта в диалоговом окне **региональные и языковые параметры** .</span><span class="sxs-lookup"><span data-stu-id="4c616-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="4c616-234">Чтобы задать язык, перейдите на вкладку **форматы** и выберите язык в поле со списком **текущий формат** .</span><span class="sxs-lookup"><span data-stu-id="4c616-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="4c616-235">Чтобы задать регион, перейдите на вкладку **Расположение** и выберите регион из поля со списком **Текущее расположение** .</span><span class="sxs-lookup"><span data-stu-id="4c616-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="4c616-236">Кроме того, для магазинов, требующих установки подключаемого модуля или специального программного обеспечения для хранения, может потребоваться изменить языковой стандарт системы на язык локали магазина, чтобы упростить установку.</span><span class="sxs-lookup"><span data-stu-id="4c616-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="4c616-237">Установщик программного обеспечения должен поддерживать как однобайтовые, так и двухбайтовые символы, и они должны выполняться в любом языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="4c616-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="4c616-238">Необходимо проверить в собственном языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="4c616-238">You must test in the native locale.</span></span> <span data-ttu-id="4c616-239">Чтобы задать собственный языковой стандарт, откройте диалоговое окно **язык и** региональные параметры, перейдите на вкладку **Администрирование** и нажмите кнопку **изменить языковой стандарт системы** , как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="4c616-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="4c616-240">Нажатие этой кнопки приводит к отображению диалогового окна **Параметры регионов и языка** .</span><span class="sxs-lookup"><span data-stu-id="4c616-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="4c616-241">Поле со списком **текущего языкового стандарта системы** в этом диалоговом окне изменяет языковой стандарт системы.</span><span class="sxs-lookup"><span data-stu-id="4c616-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="4c616-242">На следующих снимках экрана показаны вкладки, на которых можно задать регион и язык:</span><span class="sxs-lookup"><span data-stu-id="4c616-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![снимок экрана диалогового окна "региональные и языковые параметры"](images/reg-lang-opt.png)

    ![снимок экрана, показывающий, как изменить текущий язык системы](images/reg-lang-settings.png)

3.  <span data-ttu-id="4c616-245">Отключите представление информационного центра магазина, настроив проигрыватель Windows Media для воспроизведения визуализации.</span><span class="sxs-lookup"><span data-stu-id="4c616-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="4c616-246">Основное различие между платформами заключается в том, что в проигрывателе Windows Media 11 вы начинаете с выбора пункта **Воспроизведение**, а в проигрывателе Windows Media 12 — щелкнув правой кнопкой мыши главное окно.</span><span class="sxs-lookup"><span data-stu-id="4c616-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="4c616-247">На следующем снимке экрана показана последовательность параметров меню, воспроизводящих визуализацию в проигрывателе Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4c616-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![снимок экрана, показывающий, как воспроизвести визуализацию в проигрывателе Windows Media 11](images/wmp11-visual.png)

    <span data-ttu-id="4c616-249">На следующем снимке экрана показана последовательность параметров меню, воспроизводящих визуализацию в проигрывателе Windows Media 12.</span><span class="sxs-lookup"><span data-stu-id="4c616-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![снимок экрана, показывающий, как воспроизвести визуализацию в проигрывателе Windows Media 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="4c616-251">Настройка магазина</span><span class="sxs-lookup"><span data-stu-id="4c616-251">Setting Up a Store</span></span>

<span data-ttu-id="4c616-252">Сначала выполните следующие действия, чтобы настроить магазин, а затем выполните действия, описанные в следующих шагах, чтобы проверить настройку магазина:</span><span class="sxs-lookup"><span data-stu-id="4c616-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="4c616-253">Запустите проигрыватель Windows Media и подождите несколько секунд, чтобы получить последний файл AllServices.xml.</span><span class="sxs-lookup"><span data-stu-id="4c616-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="4c616-254">В Windows XP и Windows Vista для выбора Интернет-магазина сначала перейдите на вкладку, которая разделяется между представлением "Путеводитель мультимедиа" и "Интернет-магазины".</span><span class="sxs-lookup"><span data-stu-id="4c616-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="4c616-255">Затем в меню выберите пункт **Обзор всех интернет-магазинов** и выберите магазин, щелкнув его значок в списке магазинов.</span><span class="sxs-lookup"><span data-stu-id="4c616-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="4c616-256">В Windows 7 нажмите кнопку в области навигации "Библиотека", которая разделяется между кнопками " **Путеводитель" мультимедиа** "и" **Интернет-магазины** ".</span><span class="sxs-lookup"><span data-stu-id="4c616-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="4c616-257">Затем в меню выберите пункт **Обзор всех интернет-магазинов** и выберите магазин, щелкнув его значок в списке магазинов.</span><span class="sxs-lookup"><span data-stu-id="4c616-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="4c616-258">На следующем снимке экрана показано, как выбрать Интернет-магазин в проигрывателе Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![снимок экрана, показывающий, как выбрать Интернет-магазин в проигрывателе Windows Media 11](images/wmp11-set-store.png)

    <span data-ttu-id="4c616-260">На следующем снимке экрана показано, как выбрать Интернет-магазин в проигрывателе Windows Media 12:</span><span class="sxs-lookup"><span data-stu-id="4c616-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![снимок экрана, показывающий, как выбрать Интернет-магазин в проигрывателе Windows Media 12](images/wmp12-set-store.png)

3.  <span data-ttu-id="4c616-262">Следуйте инструкциям из магазина, чтобы установить дополнительное программное обеспечение, необходимое для использования магазина.</span><span class="sxs-lookup"><span data-stu-id="4c616-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="4c616-263">**Проверка настройки магазина**</span><span class="sxs-lookup"><span data-stu-id="4c616-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="4c616-264">Убедитесь, что программное обеспечение установлено.</span><span class="sxs-lookup"><span data-stu-id="4c616-264">Verify that the software installs.</span></span>

    <span data-ttu-id="4c616-265">Убедитесь, что подключаемый модуль OCX или другое программное обеспечение из магазина скачивает и устанавливает без ошибок.</span><span class="sxs-lookup"><span data-stu-id="4c616-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="4c616-266">Убедитесь, что программное обеспечение удаляется.</span><span class="sxs-lookup"><span data-stu-id="4c616-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="4c616-267">Убедитесь, что на панели управления в элементе " **программы и компоненты** " в списке " **Удалить" или "изменить программу** " отображается программное обеспечение, которое установлено в магазине, и убедитесь, что его можно удалить из списка без ошибок.</span><span class="sxs-lookup"><span data-stu-id="4c616-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="4c616-268">Убедитесь, что программное обеспечение не выполняется в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4c616-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="4c616-269">Убедитесь, что ни одно из программ из магазина не добавляет значки в область уведомлений о программе (на панели задач слева от часов) до согласия клиента на загрузку программного обеспечения магазина.</span><span class="sxs-lookup"><span data-stu-id="4c616-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="4c616-270">В основном хранилище не должно требовать установки дополнительного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4c616-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="4c616-271">Должен быть доступен базовый интерфейс мультимедиа, например потоковая передача мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c616-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="4c616-272">В некоторых магазинах устанавливается дополнительное программное обеспечение, например диспетчеры загрузки, для работы с мультимедийными файлами уровня Premier. Эти магазины могут иметь значки в области уведомлений, если значки представляют приложения, которые отделены от проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="4c616-273">Убедитесь, что вкладка хранилище работает.</span><span class="sxs-lookup"><span data-stu-id="4c616-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="4c616-274">Убедитесь, что вкладка магазин изменилась, чтобы показать выбранное хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c616-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="4c616-275">Для Windows XP и Windows Vista с проигрывателем Windows Media 11 убедитесь, что имя и значок магазина видны на фоне темного проигрывателя Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4c616-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="4c616-276">Для Windows 7 с проигрывателем Windows Media 12, убедитесь, что имя и значок магазина отображаются в области навигации "Библиотека" в контекстном меню "Сервис-Selector".</span><span class="sxs-lookup"><span data-stu-id="4c616-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="4c616-277">Убедитесь, что хранилище указано в верхней части списка выбора магазина в меню.</span><span class="sxs-lookup"><span data-stu-id="4c616-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="4c616-278">Если магазин Type 2 является рекомендуемым хранилищем (по умолчанию) для региона, то команда **Добавить текущую службу в меню** будет отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="4c616-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="4c616-279">На следующем снимке экрана показано меню, отображаемое при щелчке вкладки в правом верхнем углу проигрывателя Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![снимок экрана, отображающий вкладку "магазин" в проигрывателе Windows Media 11](images/wmp11-verify-store.png)

    <span data-ttu-id="4c616-281">На следующем снимке экрана показано меню, которое появляется при нажатии кнопки разделить в левом нижнем углу проигрывателя Windows Media 12:</span><span class="sxs-lookup"><span data-stu-id="4c616-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![снимок экрана, отображающий вкладку "магазин" в проигрывателе Windows Media 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="4c616-283">Создание учетной записи</span><span class="sxs-lookup"><span data-stu-id="4c616-283">Creating an Account</span></span>

<span data-ttu-id="4c616-284">**Проверка настройки учетной записи**</span><span class="sxs-lookup"><span data-stu-id="4c616-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="4c616-285">Убедитесь, что в магазине есть возможность создать новую учетную запись, а затем следуйте инструкциям по хранению, чтобы создать новую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4c616-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="4c616-286">На следующем снимке экрана показана кнопка **создать новую учетную запись** , так как она может появиться в проигрывателе Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![снимок экрана, показывающий, как проверить настройку учетной записи для проигрывателя Windows Media 11](images/wmp11-verify-account.png)

    <span data-ttu-id="4c616-288">На следующем снимке экрана показана кнопка **создать новую учетную запись** , так как она может появиться в проигрывателе Windows Media 12:</span><span class="sxs-lookup"><span data-stu-id="4c616-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![снимок экрана, показывающий, как проверить настройку учетной записи для проигрывателя Windows Media 12](images/wmp12-verify-account.png)

2.  <span data-ttu-id="4c616-290">Убедитесь, что вы можете войти в созданную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4c616-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="4c616-291">Настройка кэширования учетных данных</span><span class="sxs-lookup"><span data-stu-id="4c616-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="4c616-292">Сначала выполните следующие действия, чтобы настроить кэширование учетных данных, а затем выполните действия, описанные в следующих шагах, чтобы проверить настройку кэширования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="4c616-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="4c616-293">На странице входа введите учетные данные и выберите параметр сохранения сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="4c616-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="4c616-294">Убедитесь, что на странице входа установлен флажок, позволяющий пользователю кэшировать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="4c616-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="4c616-295">Дополнительное кэширование учетных данных является важной точкой безопасности.</span><span class="sxs-lookup"><span data-stu-id="4c616-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="4c616-296">Автоматическое кэширование учетных данных может предоставлять персональные данные пользователей, которые входят в общий или общедоступный компьютер.</span><span class="sxs-lookup"><span data-stu-id="4c616-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="4c616-297">Необходимо защитить сведения о клиенте, установив флажок, который отображает кэширование необязательно.</span><span class="sxs-lookup"><span data-stu-id="4c616-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="4c616-298">**Проверка кэширования учетных данных**</span><span class="sxs-lookup"><span data-stu-id="4c616-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="4c616-299">Убедитесь, что в хранилище установлен флажок **сохранить сведения о пользователе** .</span><span class="sxs-lookup"><span data-stu-id="4c616-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="4c616-300">Закройте проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="4c616-301">Повторно откройте проигрыватель Windows Media и попытайтесь скачать некоторое содержимое.</span><span class="sxs-lookup"><span data-stu-id="4c616-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="4c616-302">Убедитесь, что кэширование учетных данных имеется и работает.</span><span class="sxs-lookup"><span data-stu-id="4c616-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="4c616-303">Выйдите из магазина.</span><span class="sxs-lookup"><span data-stu-id="4c616-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="4c616-304">Закройте проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="4c616-305">Повторно откройте проигрыватель Windows Media и попытайтесь скачать некоторое содержимое.</span><span class="sxs-lookup"><span data-stu-id="4c616-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="4c616-306">Убедитесь, что пользователю предлагается ввести учетные данные, если они не кэшированы.</span><span class="sxs-lookup"><span data-stu-id="4c616-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="4c616-307">После выхода из системы и последующей попытки использования магазина клиент должен получить запрос на ввод учетных данных.</span><span class="sxs-lookup"><span data-stu-id="4c616-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="4c616-308">Получение содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-308">Content Acquisition</span></span>

<span data-ttu-id="4c616-309">В этом разделе описываются различные способы получения содержимого и проверки того, что содержимое было получено.</span><span class="sxs-lookup"><span data-stu-id="4c616-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="4c616-310">Потоковая передача содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-310">Streaming Content</span></span>

<span data-ttu-id="4c616-311">Потоковая передача всех доступных типов содержимого из хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c616-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="4c616-312">Например, потоковый Радио, видео, аудио и предварительный просмотр содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c616-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="4c616-313">**Проверка потокового содержимого**</span><span class="sxs-lookup"><span data-stu-id="4c616-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="4c616-314">Убедитесь, что все доступные типы потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c616-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="4c616-315">Убедитесь, что содержимое воспроизводится проигрывателем Windows Media Player, а не другим проигрывателем или элементом управления.</span><span class="sxs-lookup"><span data-stu-id="4c616-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="4c616-316">Получение содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-316">Obtaining Content</span></span>

<span data-ttu-id="4c616-317">Сначала выполните следующие действия, чтобы приобрести содержимое, а затем выполните действия, описанные в следующих шагах, чтобы проверить приобретение и убедиться, что содержимое загружено:</span><span class="sxs-lookup"><span data-stu-id="4c616-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="4c616-318">Запустите проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="4c616-319">Войдите в тестовую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4c616-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="4c616-320">Перейдите к содержимому для покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="4c616-321">Выполните процедуру, относящуюся к магазину, чтобы приобрести содержимое.</span><span class="sxs-lookup"><span data-stu-id="4c616-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="4c616-322">**Проверка приобретенного и скачанного содержимого**</span><span class="sxs-lookup"><span data-stu-id="4c616-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="4c616-323">Убедитесь, что вычисленная цена правильная.</span><span class="sxs-lookup"><span data-stu-id="4c616-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="4c616-324">Убедитесь, что указана правильная цена, особенно при покупке нескольких фрагментов содержимого одновременно, и убедитесь, что все сведения о балансе учетной записи обновлены правильно после покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="4c616-325">Часть содержимого можно приобрести как отдельные дорожки, а некоторые — только альбомы.</span><span class="sxs-lookup"><span data-stu-id="4c616-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="4c616-326">Убедитесь, что цена альбома не превышает сумму отдельных дорожек.</span><span class="sxs-lookup"><span data-stu-id="4c616-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="4c616-327">Убедитесь, что приобретенное содержимое загружается в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="4c616-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="4c616-328">После завершения загрузки перейдите к загруженному содержимому в библиотеке проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="4c616-329">Загруженное содержимое находится в библиотеке текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c616-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="4c616-330">Для Windows XP и Windows Vista с проигрывателем Windows Media 11 загруженное содержимое отображается в области навигации библиотеки в разделе **Библиотека** сведения, а затем в разделе **песни**.</span><span class="sxs-lookup"><span data-stu-id="4c616-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="4c616-331">Для Windows 7 с проигрывателем Windows Media 12 содержимое, загружаемое в библиотеку проигрывателя Windows Media, отображается в области навигации проигрывателя Windows Media в разделе **музыка**.</span><span class="sxs-lookup"><span data-stu-id="4c616-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="4c616-332">Убедитесь, что скачивание метаданных для покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="4c616-333">Убедитесь, что в библиотеке проигрывателя Windows Media отображаются следующие столбцы (добавьте их, если нет):</span><span class="sxs-lookup"><span data-stu-id="4c616-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="4c616-334">Исполнитель альбома</span><span class="sxs-lookup"><span data-stu-id="4c616-334">Album Artist</span></span>
    -   <span data-ttu-id="4c616-335">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4c616-335">Title</span></span>
    -   <span data-ttu-id="4c616-336">Название альбома</span><span class="sxs-lookup"><span data-stu-id="4c616-336">Album Title</span></span>
    -   <span data-ttu-id="4c616-337">Поставщик содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-337">Content Provider</span></span>
    -   <span data-ttu-id="4c616-338">Genre</span><span class="sxs-lookup"><span data-stu-id="4c616-338">Genre</span></span>

    <span data-ttu-id="4c616-339">Предыдущие столбцы должны быть заполнены.</span><span class="sxs-lookup"><span data-stu-id="4c616-339">The preceding columns must be populated.</span></span> <span data-ttu-id="4c616-340">Содержимое должно иметь обложку альбома.</span><span class="sxs-lookup"><span data-stu-id="4c616-340">Content should have album art.</span></span> <span data-ttu-id="4c616-341">Однако для прохождения проверочного тестирования не требуется Обложка альбома.</span><span class="sxs-lookup"><span data-stu-id="4c616-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="4c616-342">Убедитесь, что права на использование мультимедиа указаны правильно для покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="4c616-343">Для каждой скачанной записи щелкните правой кнопкой мыши запись и выберите пункт **Свойства**, а затем перейдите на вкладку **права использования мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="4c616-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="4c616-344">Хранилище может защищать содержимое с правами на использование мультимедиа или не защищать содержимое.</span><span class="sxs-lookup"><span data-stu-id="4c616-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="4c616-345">Вкладка **права использования мультимедиа** отражает это состояние, выполняя список ограничений или указывая, что содержимое не защищено.</span><span class="sxs-lookup"><span data-stu-id="4c616-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="4c616-346">Магазин должен сообщить наиболее актуальный план для прав на использование мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c616-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="4c616-347">Необходимо проверить фактические результаты в соответствии с ожидаемым поведением.</span><span class="sxs-lookup"><span data-stu-id="4c616-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="4c616-348">Лицензии на права на носители должны быть предварительно доставлены.</span><span class="sxs-lookup"><span data-stu-id="4c616-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="4c616-349">Клиент не должен быть необходим для воспроизведения содержимого или для получения лицензии другим процессом.</span><span class="sxs-lookup"><span data-stu-id="4c616-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="4c616-350">Необходимо сравнить конкретные права на использование носителя с тем, что хранилище передает клиенту.</span><span class="sxs-lookup"><span data-stu-id="4c616-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="4c616-351">Права должны быть переданы по меньшей мере на два других компьютера.</span><span class="sxs-lookup"><span data-stu-id="4c616-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="4c616-352">Клиенты должны иметь возможность записывать и синхронизировать свои носители.</span><span class="sxs-lookup"><span data-stu-id="4c616-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="4c616-353">На следующем снимке экрана показаны права на использование мультимедиа защищенного файла:</span><span class="sxs-lookup"><span data-stu-id="4c616-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![снимок экрана с правами на использование мультимедиа для защищенного файла](images/media-rights-protected.png)

    <span data-ttu-id="4c616-355">Если содержимое не защищено, на вкладке **права использования мультимедиа** указывается этот факт.</span><span class="sxs-lookup"><span data-stu-id="4c616-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="4c616-356">На следующем снимке экрана показаны права на использование мультимедиа незащищенного файла:</span><span class="sxs-lookup"><span data-stu-id="4c616-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![снимок экрана с правами на использование мультимедиа для незащищенного файла](images/media-rights-not-protected.png)

5.  <span data-ttu-id="4c616-358">Убедитесь, что приобретенное содержимое будет воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="4c616-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="4c616-359">Убедитесь, что загруженное содержимое воспроизводится в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="4c616-360">Воспроизведите все содержимое, приобретенное в магазине и размещенное в локальной библиотеке, или помещаете предварительную версию в поток.</span><span class="sxs-lookup"><span data-stu-id="4c616-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="4c616-361">Чтобы приобрести содержимое в Windows XP и Windows Vista с проигрывателем Windows Media 11, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4c616-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="4c616-362">Перейдите на вкладку **Воспроизведение** .</span><span class="sxs-lookup"><span data-stu-id="4c616-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="4c616-363">На панели списка наведите указатель мыши на пункт Обложка альбома, чтобы отобразить ссылку **купить** .</span><span class="sxs-lookup"><span data-stu-id="4c616-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="4c616-364">Нажмите кнопку **купить**.</span><span class="sxs-lookup"><span data-stu-id="4c616-364">Click **Buy**.</span></span>

    <span data-ttu-id="4c616-365">На следующем снимке экрана показано расположение ссылки на **покупку** в проигрывателе Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![снимок экрана, показывающий, как купить содержимое в проигрывателе Windows Media 11](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="4c616-367">Чтобы приобрести содержимое в Windows 7 с проигрывателем Windows Media 12, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4c616-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="4c616-368">В режиме библиотеки перейдите на вкладку **Воспроизведение** .</span><span class="sxs-lookup"><span data-stu-id="4c616-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="4c616-369">В списке воспроизведения на обложке альбома щелкните **магазин** .</span><span class="sxs-lookup"><span data-stu-id="4c616-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="4c616-370">На следующем снимке экрана показано, как купить содержимое в проигрывателе Windows Media 12:</span><span class="sxs-lookup"><span data-stu-id="4c616-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![снимок экрана, показывающий, как купить содержимое в проигрывателе Windows Media 12](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="4c616-372">Убедитесь, что в магазине щелкнуть **купить** **или купить** коммутаторы.</span><span class="sxs-lookup"><span data-stu-id="4c616-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="4c616-373">Проигрыватель Windows Media должен перейти к хранилищу в представлении библиотеки и загрузить магазин магазина.</span><span class="sxs-lookup"><span data-stu-id="4c616-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="4c616-374">Затем необходимо приобретать эту запись.</span><span class="sxs-lookup"><span data-stu-id="4c616-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="4c616-375">Убедитесь, что после нажатия кнопки **купить** **или купить** загружаются материалы.</span><span class="sxs-lookup"><span data-stu-id="4c616-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="4c616-376">Убедитесь, что права на использование мультимедиа соответствуют приобретенному содержимому и его метаданным, и убедитесь, что эта запись воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="4c616-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="4c616-377">Как правило, этот метод покупки должен иметь те же результаты, что и другие методы.</span><span class="sxs-lookup"><span data-stu-id="4c616-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="4c616-378">Запись содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-378">Burning Content</span></span>

<span data-ttu-id="4c616-379">Сначала выполните следующие действия для записи приобретенного содержимого (копирование приобретенного содержимого на записываемый компакт-диск или DVD-диск), а затем выполните действия, описанные в следующих шагах, чтобы убедиться, что содержимое записывается:</span><span class="sxs-lookup"><span data-stu-id="4c616-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="4c616-380">Перед записью приобретенной дорожки запишите число записанных записей, чтобы позже можно было проверить, уменьшается ли число после записи дорожки.</span><span class="sxs-lookup"><span data-stu-id="4c616-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="4c616-381">Перейдите на вкладку **запись**</span><span class="sxs-lookup"><span data-stu-id="4c616-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="4c616-382">Перетащите приобретенные дорожки в **список записи**.</span><span class="sxs-lookup"><span data-stu-id="4c616-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="4c616-383">Нажмите кнопку **начать запись** .</span><span class="sxs-lookup"><span data-stu-id="4c616-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="4c616-384">На следующем снимке экрана показан **список записи** в правой части экрана и кнопка **начать запись** под **списком записи** в проигрывателе Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![снимок экрана, показывающий, как записать содержимое в проигрывателе Windows Media 11](images/wmp11-verify-burn.png)

<span data-ttu-id="4c616-386">На следующем снимке экрана показано, как список записи отображается в проигрывателе Windows Media 12 после перетаскивания дорожки в список записи, после чего в верхней части вкладки **запись** отображается кнопка **начать запись** .</span><span class="sxs-lookup"><span data-stu-id="4c616-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![снимок экрана, показывающий, как записать содержимое в проигрывателе Windows Media 12](images/wmp12-verify-burn.png)

<span data-ttu-id="4c616-388">**Проверка возможности записи приобретенного содержимого**</span><span class="sxs-lookup"><span data-stu-id="4c616-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="4c616-389">Убедитесь, что приобретенное содержимое записывается путем воспроизведения компакт-диска или DVD-диска после завершения записи.</span><span class="sxs-lookup"><span data-stu-id="4c616-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="4c616-390">Убедитесь, что счетчик записи уменьшен.</span><span class="sxs-lookup"><span data-stu-id="4c616-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="4c616-391">Перейдите в библиотеку и откройте права использования мультимедиа для приобретенной записи, которая была записана.</span><span class="sxs-lookup"><span data-stu-id="4c616-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="4c616-392">Если число записей, которое можно записать, ограничено, убедитесь, что это число уменьшается после того, как запись будет записана.</span><span class="sxs-lookup"><span data-stu-id="4c616-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="4c616-393">Передача содержимого</span><span class="sxs-lookup"><span data-stu-id="4c616-393">Transferring Content</span></span>

<span data-ttu-id="4c616-394">Перенос содержимого на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="4c616-394">Transfer content to another computer.</span></span>

<span data-ttu-id="4c616-395">**Проверка возможности передачи приобретенного содержимого на другой компьютер**</span><span class="sxs-lookup"><span data-stu-id="4c616-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="4c616-396">Если хранилище позволяет передавать содержимое на другой компьютер, перенесите его по меньшей мере на два компьютера.</span><span class="sxs-lookup"><span data-stu-id="4c616-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="4c616-397">Сначала выполните следующие действия для синхронизации с устройством и передачи приобретенного содержимого на это устройство, а затем выполните действия, описанные в следующих шагах, чтобы убедиться, что содержимое передано:</span><span class="sxs-lookup"><span data-stu-id="4c616-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="4c616-398">Перед переносом приобретенной записи Обратите внимание на число синхронизаций, чтобы позже можно было проверить, уменьшается ли значение счетчика после перемещения курса.</span><span class="sxs-lookup"><span data-stu-id="4c616-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="4c616-399">Подключите устройство с помощью безопасного времени.</span><span class="sxs-lookup"><span data-stu-id="4c616-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="4c616-400">К примерам относятся устройства, использующие Windows Media DRM для портативных устройств, например, портативный Media Center, такие как Иривер H10, Creative Zen и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c616-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="4c616-401">В проигрывателе Windows Media откройте вкладку **Синхронизация** .</span><span class="sxs-lookup"><span data-stu-id="4c616-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="4c616-402">Перетащите содержимое из библиотеки в область **список синхронизации** на вкладке **Синхронизация** .</span><span class="sxs-lookup"><span data-stu-id="4c616-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="4c616-403">Нажмите кнопку **начать синхронизацию** .</span><span class="sxs-lookup"><span data-stu-id="4c616-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="4c616-404">На следующем снимке экрана показана запись 1 в области **списка синхронизация** и отображается кнопка **начать синхронизацию** в проигрывателе Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![снимок экрана, показывающий, как передавать содержимое в проигрывателе Windows Media 11](images/wmp11-verify-transfer.png)

<span data-ttu-id="4c616-406">На следующем снимке экрана показана запись 1 в области **списка синхронизация** и отображается кнопка **начать синхронизацию** в проигрывателе Windows Media 12:</span><span class="sxs-lookup"><span data-stu-id="4c616-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![снимок экрана, показывающий, как передавать содержимое в проигрывателе Windows Media 12](images/wmp12-verify-transfer.png)

<span data-ttu-id="4c616-408">**Проверка возможности передачи приобретенного содержимого на другое устройство**</span><span class="sxs-lookup"><span data-stu-id="4c616-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="4c616-409">Убедитесь, что приобретенное содержимое передается на устройство, воспроизводящим содержимое на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4c616-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="4c616-410">Переданное содержимое также должно иметь соответствующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="4c616-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="4c616-411">Убедитесь, что счетчик синхронизации уменьшен.</span><span class="sxs-lookup"><span data-stu-id="4c616-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="4c616-412">Перейдите к библиотеке и откройте права использования мультимедиа для передаваемой записи.</span><span class="sxs-lookup"><span data-stu-id="4c616-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="4c616-413">Если количество синхронизаций между дорожками ограничено, убедитесь, что это число уменьшается при передаче записи.</span><span class="sxs-lookup"><span data-stu-id="4c616-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="4c616-414">Функции магазина</span><span class="sxs-lookup"><span data-stu-id="4c616-414">Store Features</span></span>

<span data-ttu-id="4c616-415">В следующих разделах описывается тестирование различных функций встроенного Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="4c616-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="4c616-416">Управление учетной записью</span><span class="sxs-lookup"><span data-stu-id="4c616-416">Managing an Account</span></span>

<span data-ttu-id="4c616-417">Войдите с помощью учетной записи, которая выполнила некоторые покупки, и откройте журнал приобретений.</span><span class="sxs-lookup"><span data-stu-id="4c616-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="4c616-418">**Проверка журнала приобретений**</span><span class="sxs-lookup"><span data-stu-id="4c616-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="4c616-419">Убедитесь, что История приобретений отслеживает предыдущие покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="4c616-420">Если тип хранилища или учетной записи поддерживает эту функцию, попытайтесь восстановить удаленную покупку.</span><span class="sxs-lookup"><span data-stu-id="4c616-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="4c616-421">**Проверка возможности повторного получения предыдущих покупок**</span><span class="sxs-lookup"><span data-stu-id="4c616-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="4c616-422">Убедитесь, что возможно восстановление предыдущей покупки.</span><span class="sxs-lookup"><span data-stu-id="4c616-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="4c616-423">Если хранилище поддерживает использование нескольких компьютеров с учетной записью, проверьте все функциональные возможности, предоставляемые этой функцией.</span><span class="sxs-lookup"><span data-stu-id="4c616-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="4c616-424">**Проверка управления несколькими компьютерами с помощью одной учетной записи**</span><span class="sxs-lookup"><span data-stu-id="4c616-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="4c616-425">Проверьте функциональность хранилища для управления несколькими компьютерами.</span><span class="sxs-lookup"><span data-stu-id="4c616-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="4c616-426">Управление учетной записью Store-Specific</span><span class="sxs-lookup"><span data-stu-id="4c616-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="4c616-427">В магазине могут отсутствовать стандартные типы учетных записей, ограничения или содержимое.</span><span class="sxs-lookup"><span data-stu-id="4c616-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="4c616-428">Например, магазину, для которого требуется потоковая передача, потребуется пользовательский интерфейс для показа активных напрокат, и этот пользовательский интерфейс должен быть протестирован.</span><span class="sxs-lookup"><span data-stu-id="4c616-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="4c616-429">Хотя корпорация Майкрософт не может сертифицировать функции учетной записи, зависящей от магазина, чтобы обеспечить хорошую работу клиентов, следует протестировать эту функциональность.</span><span class="sxs-lookup"><span data-stu-id="4c616-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="4c616-430">Управление информационным центром</span><span class="sxs-lookup"><span data-stu-id="4c616-430">Managing the Info Center</span></span>

<span data-ttu-id="4c616-431">Сначала выполните следующие действия, чтобы подготовиться к тестированию состояния по умолчанию, а затем выполните следующий шаг, следующий за начальными шагами, чтобы убедиться, что центр информации по умолчанию отключен:</span><span class="sxs-lookup"><span data-stu-id="4c616-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="4c616-432">Воспроизведите некоторое содержимое из магазина.</span><span class="sxs-lookup"><span data-stu-id="4c616-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="4c616-433">Переключитесь в режим "сейчас воспроизведения".</span><span class="sxs-lookup"><span data-stu-id="4c616-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="4c616-434">В Windows XP или Windows Vista с проигрывателем Windows Media 11 перейдите на вкладку **Воспроизведение** . В Windows 7 с проигрывателем Windows Media 12 нажмите кнопку **Переключиться в** режим "сейчас" в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="4c616-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="4c616-435">**Проверка того, что центр сведений отключен по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="4c616-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="4c616-436">Убедитесь, что центр информации по умолчанию отключен.</span><span class="sxs-lookup"><span data-stu-id="4c616-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="4c616-437">Если магазин предлагает представление информационного центра, воспроизводите некоторое содержимое из магазина и пока содержимое воспроизводится, переключитесь в режим "сейчас" и включите центр информации.</span><span class="sxs-lookup"><span data-stu-id="4c616-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="4c616-438">В Windows XP или Windows Vista с проигрывателем Windows Media 11 щелкните правой кнопкой мыши в воспроизводимом окне, а затем в контекстном меню выберите **представление центра сведений**.</span><span class="sxs-lookup"><span data-stu-id="4c616-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="4c616-439">На следующем снимке экрана показано контекстное меню в проигрывателе Windows Media 11:</span><span class="sxs-lookup"><span data-stu-id="4c616-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![снимок экрана, показывающий, как получить доступ к информационному центру магазина в проигрывателе Windows Media 11](images/wmp11-info-center.png)

<span data-ttu-id="4c616-441">В Windows 7 с проигрывателем Windows Media 12 щелкните правой кнопкой мыши воспроизводимое окно, в контекстном меню выберите **визуализации**, а затем — **представление центра сведений**.</span><span class="sxs-lookup"><span data-stu-id="4c616-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="4c616-442">На следующем снимке экрана показано контекстное меню проигрывателя Windows Media 12:</span><span class="sxs-lookup"><span data-stu-id="4c616-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![снимок экрана, показывающий, как получить доступ к информационному центру магазина в проигрывателе Windows Media 12](images/wmp12-info-center.png)

<span data-ttu-id="4c616-444">**Проверка работоспособности информационного центра**</span><span class="sxs-lookup"><span data-stu-id="4c616-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="4c616-445">Убедитесь, что в информационном центре отображаются сведения о файлах мультимедиа в области немедленного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4c616-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="4c616-446">На следующем снимке экрана показан пример таких сведений о мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="4c616-446">The following screen shot shows an example of such media information:</span></span>

    ![снимок экрана, показывающий функциональные возможности информационного центра магазина](images/media-information.png)

<span data-ttu-id="4c616-448">Если на странице имеются ссылки на покупки или другие ссылки, щелкните ссылки.</span><span class="sxs-lookup"><span data-stu-id="4c616-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="4c616-449">**Проверка ссылок в представлении центра сведений**</span><span class="sxs-lookup"><span data-stu-id="4c616-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="4c616-450">Убедитесь, что в ссылках отображается хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c616-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="4c616-451">Проигрыватель Windows Media должен переключиться в хранилище в своей библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4c616-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="4c616-452">Взаимодействие с магазином</span><span class="sxs-lookup"><span data-stu-id="4c616-452">Store Interaction</span></span>

<span data-ttu-id="4c616-453">В следующих разделах описывается, как проверить взаимодействие между другими магазинами и тестируемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="4c616-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="4c616-454">Возврат в активное хранилище</span><span class="sxs-lookup"><span data-stu-id="4c616-454">Yielding to the Active Store</span></span>

<span data-ttu-id="4c616-455">Переключитесь в хранилище, отличное от тестируемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c616-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="4c616-456">**Проверка возврата в активное хранилище**</span><span class="sxs-lookup"><span data-stu-id="4c616-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="4c616-457">Убедитесь, что проверенное хранилище выдает активное хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c616-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="4c616-458">Предотвращение того, что проверенное хранилище будет переделаться через активное хранилище</span><span class="sxs-lookup"><span data-stu-id="4c616-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="4c616-459">Выбрав другое хранилище, закройте проигрыватель Windows Media и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="4c616-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="4c616-460">Запустите проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c616-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="4c616-461">**Проверка того, что проверенное хранилище не занимает больше**</span><span class="sxs-lookup"><span data-stu-id="4c616-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="4c616-462">Убедитесь, что отображается последнее активное хранилище и что проверенное хранилище не отображается.</span><span class="sxs-lookup"><span data-stu-id="4c616-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="4c616-463">Доступ к хранилищу в режиме High-Contrast</span><span class="sxs-lookup"><span data-stu-id="4c616-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="4c616-464">Сначала включите режим высокой контрастности, нажав левую клавишу SHIFT + левый ALT + PRINT SCREEN, а затем выполните следующие действия, чтобы проверить доступность высокой контрастности:</span><span class="sxs-lookup"><span data-stu-id="4c616-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="4c616-465">**Проверка доступности хранилища в режиме высокой контрастности**</span><span class="sxs-lookup"><span data-stu-id="4c616-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="4c616-466">Убедитесь, что пользовательский интерфейс для входа не поврежден и работает.</span><span class="sxs-lookup"><span data-stu-id="4c616-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="4c616-467">Убедитесь, что все окна и диалоговые окна отображаются правильно.</span><span class="sxs-lookup"><span data-stu-id="4c616-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="4c616-468">Приобретите носитель.</span><span class="sxs-lookup"><span data-stu-id="4c616-468">Purchase media.</span></span> <span data-ttu-id="4c616-469">Убедитесь, что отображаются кнопки покупки и загрузки, менеджеры загрузки, сведения о ценах и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c616-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="4c616-470">Убедитесь, что вы можете выполнять потоковую передачу, запись и синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="4c616-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="4c616-471">Найдите обрезанный текст и элементы пользовательского интерфейса, текст, который не является разборчиво, и другие видимые дефекты.</span><span class="sxs-lookup"><span data-stu-id="4c616-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="4c616-472">Защита хранилища</span><span class="sxs-lookup"><span data-stu-id="4c616-472">Securing a Store</span></span>

<span data-ttu-id="4c616-473">Чтобы проверить безопасность учетной записи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4c616-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="4c616-474">**Проверка безопасности учетной записи**</span><span class="sxs-lookup"><span data-stu-id="4c616-474">**To verify account security**</span></span>

1.  <span data-ttu-id="4c616-475">Введите неправильно сформированные данные учетной записи на странице входа и в диалоговом окне и убедитесь, что хранилище отклоняет его.</span><span class="sxs-lookup"><span data-stu-id="4c616-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="4c616-476">Войдите, откройте страницу учетной записи и выйдите из нее.</span><span class="sxs-lookup"><span data-stu-id="4c616-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="4c616-477">Нажмите кнопку "назад" в проигрывателе Windows Media и убедитесь, что вы не видите предыдущую информацию об учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c616-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 




