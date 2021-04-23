---
title: Общие рекомендации по переносу
description: Перенос 32-разрядных приложений в 64-разрядную версию Microsoft Windows будет проще, чем перенос 16-разрядных приложений в 32-bit Windows. Тем не менее, перемещение будет более плавным благодаря тщательному планированию. Ниже приведены некоторые общие рекомендации.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- Перенос 32-разрядных приложений в 64-разрядное программирование Windows 64
- 64-разрядное руководство по программированию для Windows, 64-разрядное программирование для Windows, рекомендации по переносу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "104273190"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="611e9-107">Общие рекомендации по переносу</span><span class="sxs-lookup"><span data-stu-id="611e9-107">General Porting Guidelines</span></span>

<span data-ttu-id="611e9-108">Перенос 32-разрядных приложений в 64-разрядную версию Microsoft Windows будет проще, чем перенос 16-разрядных приложений в 32-bit Windows.</span><span class="sxs-lookup"><span data-stu-id="611e9-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="611e9-109">Тем не менее, перемещение будет более плавным благодаря тщательному планированию.</span><span class="sxs-lookup"><span data-stu-id="611e9-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="611e9-110">Ниже приведены некоторые общие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="611e9-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="611e9-111">Планирование</span><span class="sxs-lookup"><span data-stu-id="611e9-111">Planning</span></span>

-   <span data-ttu-id="611e9-112">Определите величину усилий, требуемых для порта.</span><span class="sxs-lookup"><span data-stu-id="611e9-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="611e9-113">Оценить, сколько работы вовлечено, определив следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="611e9-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="611e9-114">Проблема с 32-битным кодом.</span><span class="sxs-lookup"><span data-stu-id="611e9-114">Problem 32-bit code.</span></span> <span data-ttu-id="611e9-115">Скомпилируйте 32-разрядный код с помощью 64-разрядного компилятора и изучите экстент ошибок и предупреждений.</span><span class="sxs-lookup"><span data-stu-id="611e9-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="611e9-116">Общие компоненты или зависимости.</span><span class="sxs-lookup"><span data-stu-id="611e9-116">Shared components or dependencies.</span></span> <span data-ttu-id="611e9-117">Определите, какие компоненты приложения берутся из других групп и планируете ли эти команды разрабатывать 64-разрядные версии кода.</span><span class="sxs-lookup"><span data-stu-id="611e9-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="611e9-118">Устаревший или код сборки.</span><span class="sxs-lookup"><span data-stu-id="611e9-118">Legacy or assembly code.</span></span> <span data-ttu-id="611e9-119">16-разрядные приложения на базе Windows не работают в 64-разрядной версии Windows и должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="611e9-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="611e9-120">Хотя код сборки x86 выполняется в WOW64, может потребоваться переписать этот код, чтобы воспользоваться преимуществами скорости архитектуры Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="611e9-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="611e9-121">Перенос всего приложения, а не только его частей.</span><span class="sxs-lookup"><span data-stu-id="611e9-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="611e9-122">Хотя можно перенести части приложения или ограничить код до 2G с помощью/LARGEADDRESSAWARE: нет, эта стратегия меняет краткосрочный выигрыш на долгосрочные.</span><span class="sxs-lookup"><span data-stu-id="611e9-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="611e9-123">/LARGEADDRESSAWARE: для двоичного файла ARM64 не учитывается.</span><span class="sxs-lookup"><span data-stu-id="611e9-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="611e9-124">Найти замены для технологий, которые не будут перенесены.</span><span class="sxs-lookup"><span data-stu-id="611e9-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="611e9-125">Некоторые технологии, включая DAO (объект доступа к данным) и ядро базы данных Jet Red, не будут перенесены в 64-разрядную версию Windows.</span><span class="sxs-lookup"><span data-stu-id="611e9-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="611e9-126">Рассматривайте 64-разрядную версию в виде отдельного выпуска продукта.</span><span class="sxs-lookup"><span data-stu-id="611e9-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="611e9-127">Несмотря на то, что ваш 64-разрядный продукт может совместно использовать ту же базу кода, что и ваша 32-разрядная версия, она требует дополнительного тестирования и может иметь другие соображения о выпуске.</span><span class="sxs-lookup"><span data-stu-id="611e9-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="611e9-128">Разработка</span><span class="sxs-lookup"><span data-stu-id="611e9-128">Development</span></span>

-   <span data-ttu-id="611e9-129">Начните разрабатывать совместимый код прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="611e9-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="611e9-130">Разработчики могут приступить к написанию совместимого кода, используя последние файлы заголовков Windows и новые типы данных без негативных последствий при разработке 32-разрядного продукта.</span><span class="sxs-lookup"><span data-stu-id="611e9-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="611e9-131">Дополнительные сведения см. в разделе [Подготовка к 64-разрядной версии Windows](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="611e9-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="611e9-132">Убедитесь, что код может быть скомпилирован как для 32, так и для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="611e9-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="611e9-133">Новая модель данных была разработана для того, чтобы разрешить сборку 32-и 64-разрядных приложений из одной базы кода с несколькими изменениями.</span><span class="sxs-lookup"><span data-stu-id="611e9-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="611e9-134">SQL Server и группы разработки Windows разрабатывают 32-и 64-разрядные версии своих продуктов из одной и той же базы кода.</span><span class="sxs-lookup"><span data-stu-id="611e9-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="611e9-135">Для лучшей производительности используйте новые функции оптимизации компилятора.</span><span class="sxs-lookup"><span data-stu-id="611e9-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="611e9-136">Оптимизация кода для процессоров Intel Itanium важнее, чем для x86.</span><span class="sxs-lookup"><span data-stu-id="611e9-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="611e9-137">Компилятор предполагает наличие многих функций оптимизации, ранее обработанных микропроцессором.</span><span class="sxs-lookup"><span data-stu-id="611e9-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="611e9-138">Вы можете максимально увеличить производительность 64-разрядного приложения, используя два новых средства оптимизации компилятора: Оптимизация с использованием *профиля* и *Оптимизация всей программы*.</span><span class="sxs-lookup"><span data-stu-id="611e9-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="611e9-139">Обе эти функции приводят к длительному времени сборки и нуждаются в ранней разработке хороших сценариев тестирования.</span><span class="sxs-lookup"><span data-stu-id="611e9-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="611e9-140">*Оптимизация, управляемая профилированием* , включает в себя двухэтапный процесс компиляции.</span><span class="sxs-lookup"><span data-stu-id="611e9-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="611e9-141">Во время первой компиляции код инструментирован для отслеживания поведения выполнения.</span><span class="sxs-lookup"><span data-stu-id="611e9-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="611e9-142">Эти сведения используются во второй компиляции для указания всех возможностей оптимизации.</span><span class="sxs-lookup"><span data-stu-id="611e9-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="611e9-143">*Оптимизация всей программы* анализирует код во всех файлах приложения, а не только в одной.</span><span class="sxs-lookup"><span data-stu-id="611e9-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="611e9-144">Такой подход повышает производительность несколькими способами, включая лучшее встраивание, а также улучшает анализ побочных эффектов и пользовательские соглашения о вызовах.</span><span class="sxs-lookup"><span data-stu-id="611e9-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="611e9-145">Тестирование</span><span class="sxs-lookup"><span data-stu-id="611e9-145">Testing</span></span>

-   <span data-ttu-id="611e9-146">Определите, выполняется ли тестирование 64 или 32-разрядного кода в эмуляторе WOW64.</span><span class="sxs-lookup"><span data-stu-id="611e9-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="611e9-147">Некоторые приложения включают в себя как машинный, так и не64 управляемый код и 32-разрядный код, выполняющиеся в WOW64.</span><span class="sxs-lookup"><span data-stu-id="611e9-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="611e9-148">Внимательно изучите это время при разработке плана тестирования и определите, должны ли средства тестирования быть 64-разрядными, 32-разрядными или комбинацией.</span><span class="sxs-lookup"><span data-stu-id="611e9-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="611e9-149">Часто требуется тестировать 64-и 32-разрядные версии приложения в 64-bit Windows.</span><span class="sxs-lookup"><span data-stu-id="611e9-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="611e9-150">Тестирование часто используемых 32-разрядных компонентов.</span><span class="sxs-lookup"><span data-stu-id="611e9-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="611e9-151">Сначала перекомпилируйте код до 64-разрядного и тестового.</span><span class="sxs-lookup"><span data-stu-id="611e9-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="611e9-152">Во-вторых, устраните проблемы, выполните повторную компиляцию в 32-бит, а затем протестируйте.</span><span class="sxs-lookup"><span data-stu-id="611e9-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="611e9-153">В-третьих, выполните повторную компиляцию до 64 бит и тест.</span><span class="sxs-lookup"><span data-stu-id="611e9-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="611e9-154">Проверьте компоненты COM и RPC.</span><span class="sxs-lookup"><span data-stu-id="611e9-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="611e9-155">Убедитесь, что как 32, так и 64-разрядные компоненты COM и RPC правильно обмениваются данными.</span><span class="sxs-lookup"><span data-stu-id="611e9-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="611e9-156">Также может потребоваться тестирование связи с 16-разрядными компонентами по сети.</span><span class="sxs-lookup"><span data-stu-id="611e9-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="611e9-157">Протестируйте 32-разрядную версию в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="611e9-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="611e9-158">Клиенты могут продолжать использовать 32-разрядные приложения на 64-разрядной версии Windows, где проблемы с производительностью и памятью не являются главными соображениями.</span><span class="sxs-lookup"><span data-stu-id="611e9-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="611e9-159">Тестирование различных конфигураций памяти.</span><span class="sxs-lookup"><span data-stu-id="611e9-159">Test different memory configurations.</span></span>

    <span data-ttu-id="611e9-160">Добавление больших объемов памяти на сервере иногда предоставляет ранее незамеченные проблемы в приложении или операционной системе.</span><span class="sxs-lookup"><span data-stu-id="611e9-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




