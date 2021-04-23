---
title: Общие сведения об API увеличения
description: В этом разделе описывается API для увеличения масштаба и объясняется его использование в приложении.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Увеличения
- приложения для увеличения масштаба экрана
- Увеличения
- обработка пользовательских изображений
- Magnification.dll
- Создание элементов управления "Экранная лупа"
- Выборочное увеличение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719134"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="bee23-110">Общие сведения об API увеличения</span><span class="sxs-lookup"><span data-stu-id="bee23-110">Magnification API Overview</span></span>

<span data-ttu-id="bee23-111">API увеличения позволяет разработчикам вспомогательных технологий разрабатывать приложения для увеличения масштаба экрана, работающие в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bee23-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="bee23-112">В этом разделе описывается API для увеличения масштаба и объясняется его использование в приложении.</span><span class="sxs-lookup"><span data-stu-id="bee23-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="bee23-113">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="bee23-113">It contains the following sections:</span></span>

- [<span data-ttu-id="bee23-114">Начало работы</span><span class="sxs-lookup"><span data-stu-id="bee23-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="bee23-115">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="bee23-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="bee23-116">Типы экранных Лупы</span><span class="sxs-lookup"><span data-stu-id="bee23-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="bee23-117">Коэффициент увеличения</span><span class="sxs-lookup"><span data-stu-id="bee23-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="bee23-118">Цветовые эффекты</span><span class="sxs-lookup"><span data-stu-id="bee23-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="bee23-119">Исходный прямоугольник</span><span class="sxs-lookup"><span data-stu-id="bee23-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="bee23-120">Список фильтров</span><span class="sxs-lookup"><span data-stu-id="bee23-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="bee23-121">Преобразование входных данных</span><span class="sxs-lookup"><span data-stu-id="bee23-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="bee23-122">Системный курсор</span><span class="sxs-lookup"><span data-stu-id="bee23-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="bee23-123">Инициализация библиотеки времени выполнения с помощью экранной лупы</span><span class="sxs-lookup"><span data-stu-id="bee23-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="bee23-124">Использование экранной лупы Full-Screen</span><span class="sxs-lookup"><span data-stu-id="bee23-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="bee23-125">Использование элемента управления "Экранная лупа"</span><span class="sxs-lookup"><span data-stu-id="bee23-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="bee23-126">Создание элемента управления "Экранная лупа"</span><span class="sxs-lookup"><span data-stu-id="bee23-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="bee23-127">Инициализация элемента управления</span><span class="sxs-lookup"><span data-stu-id="bee23-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="bee23-128">Установка исходного прямоугольника</span><span class="sxs-lookup"><span data-stu-id="bee23-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="bee23-129">Применение цветовых эффектов</span><span class="sxs-lookup"><span data-stu-id="bee23-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="bee23-130">Выборочное увеличение</span><span class="sxs-lookup"><span data-stu-id="bee23-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="bee23-131">См. также</span><span class="sxs-lookup"><span data-stu-id="bee23-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="bee23-132">Приступая к работе</span><span class="sxs-lookup"><span data-stu-id="bee23-132">Getting Started</span></span>

<span data-ttu-id="bee23-133">Первоначальный выпуск API лупы поддерживается в Windows Vista и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="bee23-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="bee23-134">В Windows 8 и более поздних версиях API-интерфейс поддерживает дополнительные функции, включая увеличение масштаба экрана и настройку видимости увеличенного системного курсора.</span><span class="sxs-lookup"><span data-stu-id="bee23-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="bee23-135">Поддержка API увеличения предоставляется Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="bee23-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="bee23-136">Чтобы скомпилировать приложение, включите увеличение. h и ссылку на увеличение. lib.</span><span class="sxs-lookup"><span data-stu-id="bee23-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="bee23-137">API увеличения не поддерживается в WOW64; то есть 32-разрядное приложение с экранной лупой не будет правильно работать в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="bee23-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="bee23-138">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="bee23-138">Basic Concepts</span></span>

<span data-ttu-id="bee23-139">В этом разделе описаны фундаментальные понятия, на которых основан API увеличения.</span><span class="sxs-lookup"><span data-stu-id="bee23-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="bee23-140">Он содержит следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="bee23-140">It contains the following parts:</span></span>

- [<span data-ttu-id="bee23-141">Типы экранных Лупы</span><span class="sxs-lookup"><span data-stu-id="bee23-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="bee23-142">Коэффициент увеличения</span><span class="sxs-lookup"><span data-stu-id="bee23-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="bee23-143">Цветовые эффекты</span><span class="sxs-lookup"><span data-stu-id="bee23-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="bee23-144">Исходный прямоугольник</span><span class="sxs-lookup"><span data-stu-id="bee23-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="bee23-145">Список фильтров</span><span class="sxs-lookup"><span data-stu-id="bee23-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="bee23-146">Преобразование входных данных</span><span class="sxs-lookup"><span data-stu-id="bee23-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="bee23-147">Системный курсор</span><span class="sxs-lookup"><span data-stu-id="bee23-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="bee23-148">Типы экранных Лупы</span><span class="sxs-lookup"><span data-stu-id="bee23-148">Types of Magnifiers</span></span>

<span data-ttu-id="bee23-149">API поддерживает два типа экранной лупы: *полноэкранный* экран и *элемент управления "Экранная лупа*".</span><span class="sxs-lookup"><span data-stu-id="bee23-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="bee23-150">Полноэкранная экранная лупа увеличивает содержимое всего экрана, а элемент управления "Экранная лупа" увеличивает содержимое определенной области экрана и отображает содержимое в окне.</span><span class="sxs-lookup"><span data-stu-id="bee23-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="bee23-151">В обеих экранах отображаются изображения и текст, и они позволяют управлять объемом увеличения.</span><span class="sxs-lookup"><span data-stu-id="bee23-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="bee23-152">К увеличенному экрану можно также применить цветовые эффекты, что облегчит их отображение для людей, имеющих цвет недостатки или требующих большего или меньшего контраста.</span><span class="sxs-lookup"><span data-stu-id="bee23-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="bee23-153">API элемента управления "Экранная лупа" доступен в Windows Vista и более поздних операционных системах, а полноэкранный API экранной лупы доступен только в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bee23-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="bee23-154">Коэффициент увеличения</span><span class="sxs-lookup"><span data-stu-id="bee23-154">Magnification Factor</span></span>

<span data-ttu-id="bee23-155">И экранная лупа, и элемент управления "Экранная лупа" применяют преобразование масштабирования для увеличения содержимого экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="bee23-156">Величина увеличения, применяемая преобразованием «масштаб», называется *коэффициентом увеличения*.</span><span class="sxs-lookup"><span data-stu-id="bee23-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="bee23-157">Он выражается в виде значения с плавающей запятой, где 1,0 соответствует без увеличения, а большие значения приводят к увеличению соответствующего объема.</span><span class="sxs-lookup"><span data-stu-id="bee23-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="bee23-158">Например, значение 1,5 делает содержимое экрана 50 процентов больше.</span><span class="sxs-lookup"><span data-stu-id="bee23-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="bee23-159">Коэффициент увеличения меньше 1,0 недопустим.</span><span class="sxs-lookup"><span data-stu-id="bee23-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="bee23-160">Цветовые эффекты</span><span class="sxs-lookup"><span data-stu-id="bee23-160">Color Effects</span></span>

<span data-ttu-id="bee23-161">Цветовые эффекты достигаются путем применения матрицы преобразования «5 в 5 цветов» к цветам увеличенного содержимого экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="bee23-162">Матрица определяет интенситиесие красного, синего, зеленого и альфа-компонентов содержимого.</span><span class="sxs-lookup"><span data-stu-id="bee23-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="bee23-163">Дополнительные сведения см. в разделе [Использование матрицы цветов для преобразования одного цвета](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) в документации по Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="bee23-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="bee23-164">Исходный прямоугольник</span><span class="sxs-lookup"><span data-stu-id="bee23-164">Source Rectangle</span></span>

<span data-ttu-id="bee23-165">Полноэкранная экранная лупа применяет преобразование «масштабирование» и «цвет» ко всему экрану.</span><span class="sxs-lookup"><span data-stu-id="bee23-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="bee23-166">С другой стороны, элемент управления "Экранная лупа" копирует область экрана, называемую *исходным прямоугольником*, в растровое изображение вне экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="bee23-167">Затем элемент управления применяет преобразование «масштаб» и преобразование «цвет» (при наличии) к растровому растру, расположенному на экране.</span><span class="sxs-lookup"><span data-stu-id="bee23-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="bee23-168">Наконец, элемент управления отображает масштабированное и цветное растровое изображение в окне элемента управления "Экранная лупа".</span><span class="sxs-lookup"><span data-stu-id="bee23-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="bee23-169">Список фильтров</span><span class="sxs-lookup"><span data-stu-id="bee23-169">Filter List</span></span>

<span data-ttu-id="bee23-170">По умолчанию элемент управления "Экранная лупа" увеличивает все окна в указанном прямоугольнике источника.</span><span class="sxs-lookup"><span data-stu-id="bee23-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="bee23-171">Однако, предоставляя *список фильтров* дескрипторов окон, можно управлять тем, какие окна включены в увеличенное содержимое, а какие — нет.</span><span class="sxs-lookup"><span data-stu-id="bee23-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="bee23-172">Дополнительные сведения см. в разделе [выборочное увеличение](#selective-magnification).</span><span class="sxs-lookup"><span data-stu-id="bee23-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="bee23-173">Полноэкранная экранная лупа не поддерживает список фильтров; Он всегда увеличивает все окна на экране.</span><span class="sxs-lookup"><span data-stu-id="bee23-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="bee23-174">Преобразование входных данных</span><span class="sxs-lookup"><span data-stu-id="bee23-174">Input Transform</span></span>

<span data-ttu-id="bee23-175">Как правило, увеличенное содержимое экрана — «невидимый» для пользовательского пера или сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="bee23-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="bee23-176">Например, если пользователь касается увеличенного изображения элемента управления, система не обязательно передает входные данные в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bee23-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="bee23-177">Вместо этого система передает входные данные какому-либо элементу (если таковой имеется), расположенному на экранах с нажатием экрана, на неувеличенном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="bee23-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="bee23-178">Функция [**магсетинпуттрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) позволяет указать *Преобразование ввода* , которое сопоставляет пространство координат увеличенного экрана с фактическим (неувеличенным) координатным пространством экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="bee23-179">Это позволяет системе передавать перо или сенсорный ввод, введенный в увеличенном содержимом экрана, в нужный элемент пользовательского интерфейса на экране.</span><span class="sxs-lookup"><span data-stu-id="bee23-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="bee23-180">Вызывающий процесс должен иметь привилегии UIAccess, чтобы задать входное преобразование.</span><span class="sxs-lookup"><span data-stu-id="bee23-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="bee23-181">Дополнительные сведения см. в разделе [вопросы безопасности модели автоматизации пользовательского интерфейса](../uiauto-securityoverview.md) и [/MANIFESTUAC (Встраивание данных контроля учетных записей в манифест)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span><span class="sxs-lookup"><span data-stu-id="bee23-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="bee23-182">Системный курсор</span><span class="sxs-lookup"><span data-stu-id="bee23-182">System Cursor</span></span>

<span data-ttu-id="bee23-183">Функция [**магшовсистемкурсор**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) позволяет отображать или скрывать системный курсор.</span><span class="sxs-lookup"><span data-stu-id="bee23-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="bee23-184">При отображении системного курсора при активной экранной лупы, системный курсор всегда будет увеличиваться вместе с остальным содержимым экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="bee23-185">Если вы скрываете системный курсор при активной экранной лупы, системный курсор не отображается вообще.</span><span class="sxs-lookup"><span data-stu-id="bee23-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="bee23-186">С помощью элемента управления "Экранная лупа" функция [**магшовсистемкурсор**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) показывает или скрывает неувеличенный системный курсор, но не влияет на увеличенный системный курсор.</span><span class="sxs-lookup"><span data-stu-id="bee23-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="bee23-187">Видимость увеличенного системного курсора зависит от того, имеет ли элемент управления "Экранная лупа" стиль [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bee23-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="bee23-188">При наличии этого стиля элемент управления "Экранная лупа" отображает увеличенный системный курсор вместе с увеличенным содержимым экрана, когда системный курсор попадает в исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="bee23-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="bee23-189">Инициализация библиотеки времени выполнения с помощью экранной лупы</span><span class="sxs-lookup"><span data-stu-id="bee23-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="bee23-190">Перед вызовом любых других функций API экранной лупы необходимо создать и инициализировать объекты времени выполнения экранной лупы, вызвав функцию [**магинитиализе**](/windows/win32/api/Magnification/nf-magnification-maginitialize) .</span><span class="sxs-lookup"><span data-stu-id="bee23-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="bee23-191">Аналогичным образом после завершения использования API экранной лупы вызовите функцию [**магунинитиализе**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) , чтобы уничтожить объекты времени выполнения экранной лупы и освободить связанные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="bee23-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="bee23-192">Использование экранной лупы Full-Screen</span><span class="sxs-lookup"><span data-stu-id="bee23-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="bee23-193">Чтобы использовать полноэкранную экранную лупу, вызовите функцию [**магсетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="bee23-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="bee23-194">Параметр *маглевел* задает коэффициент увеличения.</span><span class="sxs-lookup"><span data-stu-id="bee23-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="bee23-195">Параметры *ксоффсет* и *йоффсет* определяют, как увеличенное содержимое экрана располагается относительно экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="bee23-196">При увеличении содержимого экрана оно становится больше, чем само окно.</span><span class="sxs-lookup"><span data-stu-id="bee23-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="bee23-197">Часть содержимого выходит за края экрана и невидима для пользователя.</span><span class="sxs-lookup"><span data-stu-id="bee23-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="bee23-198">Параметры *ксоффсет* и *йоффсет* функции [**магсетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) определяют, какая часть увеличения содержимого экрана отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="bee23-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="bee23-199">Вместе параметры задают координаты точки в неувеличенном содержимом экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="bee23-200">Когда содержимое будет увеличено, оно позиционируется с указанной точкой в верхнем левом углу экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="bee23-201">В следующем примере устанавливается коэффициент увеличения для полноэкранной экранной лупы, и центр увеличенного содержимого экрана помещается в центре экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="bee23-202">Используйте функцию [**магсетфуллскринколореффект**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) , чтобы применить цветовые эффекты к полноэкранному содержимому, задав матрицу преобразования цвета, определяемую приложением.</span><span class="sxs-lookup"><span data-stu-id="bee23-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="bee23-203">Например, в следующем примере задается матрица преобразования цвета, которая преобразует цвета в градации серого.</span><span class="sxs-lookup"><span data-stu-id="bee23-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="bee23-204">Вы можете получить текущий коэффициент увеличения и значения смещения, вызвав функцию [**магжетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="bee23-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="bee23-205">Вы можете получить матрицу текущего преобразования цвета, вызвав функцию [**магжетфуллскринколореффект**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .</span><span class="sxs-lookup"><span data-stu-id="bee23-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="bee23-206">Использование элемента управления "Экранная лупа"</span><span class="sxs-lookup"><span data-stu-id="bee23-206">Using the Magnifier Control</span></span>

<span data-ttu-id="bee23-207">Элемент управления "Экранная лупа" увеличивает содержимое определенной области экрана и отображает содержимое в окне.</span><span class="sxs-lookup"><span data-stu-id="bee23-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="bee23-208">В этом разделе описывается использование элемента управления "Экранная лупа".</span><span class="sxs-lookup"><span data-stu-id="bee23-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="bee23-209">Он содержит следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="bee23-209">It contains the following parts:</span></span>

- [<span data-ttu-id="bee23-210">Создание элемента управления "Экранная лупа"</span><span class="sxs-lookup"><span data-stu-id="bee23-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="bee23-211">Инициализация элемента управления</span><span class="sxs-lookup"><span data-stu-id="bee23-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="bee23-212">Установка исходного прямоугольника</span><span class="sxs-lookup"><span data-stu-id="bee23-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="bee23-213">Применение цветовых эффектов</span><span class="sxs-lookup"><span data-stu-id="bee23-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="bee23-214">Выборочное увеличение</span><span class="sxs-lookup"><span data-stu-id="bee23-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="bee23-215">Создание элемента управления "Экранная лупа"</span><span class="sxs-lookup"><span data-stu-id="bee23-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="bee23-216">Элемент управления "Экранная лупа" должен размещаться в окне, созданном с помощью расширенного стиля [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bee23-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="bee23-217">После создания главного окна вызовите [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) , чтобы задать непрозрачность главного окна.</span><span class="sxs-lookup"><span data-stu-id="bee23-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="bee23-218">Основное окно обычно имеет значение Полная прозрачность, чтобы предотвратить отображение базового содержимого экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="bee23-219">В следующем примере показано, как задать полную непрозрачность для окна главного приложения.</span><span class="sxs-lookup"><span data-stu-id="bee23-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="bee23-220">Если применить стиль [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) к главному окну, щелчки мыши передаются в любой объект, находящийся за ведущим окном в расположении курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="bee23-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="bee23-221">Имейте в виду, что, поскольку главное окно не обрабатывает щелчки мыши, пользователь не сможет переместить или изменить размер окна лупы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="bee23-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="bee23-222">Класс Window окна элемента управления "Экранная лупа" должен быть **WC_MAGNIFIER**.</span><span class="sxs-lookup"><span data-stu-id="bee23-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="bee23-223">При применении стиля [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) элемент управления "Экранная лупа" включает системный курсор в увеличенном содержимом экрана, и этот курсор увеличен вместе с содержимым экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="bee23-224">После создания элемента управления "Экранная лупа" следует держать маркер окна, чтобы его можно было передать другим функциям.</span><span class="sxs-lookup"><span data-stu-id="bee23-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="bee23-225">В следующем примере показано, как создать элемент управления "Экранная лупа".</span><span class="sxs-lookup"><span data-stu-id="bee23-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="bee23-226">Инициализация элемента управления</span><span class="sxs-lookup"><span data-stu-id="bee23-226">Initializing the Control</span></span>

<span data-ttu-id="bee23-227">После создания элемента управления "Экранная лупа" необходимо вызвать функцию [**магсетвиндовтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) , чтобы указать коэффициент увеличения.</span><span class="sxs-lookup"><span data-stu-id="bee23-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="bee23-228">Это просто вопрос указания матрицы</span><span class="sxs-lookup"><span data-stu-id="bee23-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="bee23-229">(*n*, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="bee23-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="bee23-230">(0,0, *n*, 0,0)</span><span class="sxs-lookup"><span data-stu-id="bee23-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="bee23-231">(0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="bee23-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="bee23-232">где *n* — коэффициент увеличения.</span><span class="sxs-lookup"><span data-stu-id="bee23-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="bee23-233">В следующем примере показано, как задать коэффициент увеличения для элемента управления "Экранная лупа".</span><span class="sxs-lookup"><span data-stu-id="bee23-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="bee23-234">Установка исходного прямоугольника</span><span class="sxs-lookup"><span data-stu-id="bee23-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="bee23-235">По мере того, как пользователь перемещает курсор мыши на экран, приложение вызывает функцию [**магсетвиндовсаурце**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) , чтобы указать часть базового экрана, которая будет увеличена.</span><span class="sxs-lookup"><span data-stu-id="bee23-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="bee23-236">В приведенном ниже примере функции вычисляется расположение и размеры исходного прямоугольника (на основе расположения мыши и размеров окна экранной лупы, деленного на коэффициент увеличения) и настраивает исходный прямоугольник соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="bee23-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="bee23-237">Функция также выравнивает клиентскую область окна главного приложения в позиции мыши.</span><span class="sxs-lookup"><span data-stu-id="bee23-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="bee23-238">Эта функция будет вызываться с интервалами для обновления окна лупы.</span><span class="sxs-lookup"><span data-stu-id="bee23-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="bee23-239">Применение цветовых эффектов</span><span class="sxs-lookup"><span data-stu-id="bee23-239">Applying Color Effects</span></span>

<span data-ttu-id="bee23-240">Элемент управления "Экранная лупа", имеющий стиль [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) , применяет встроенную матрицу преобразования цвета, которая инвертирует цвета увеличенного содержимого экрана.</span><span class="sxs-lookup"><span data-stu-id="bee23-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="bee23-241">На следующем рисунке показано содержимое экрана в элементе управления "Экранная лупа" с **MS_INVERTCOLORS** стилем.</span><span class="sxs-lookup"><span data-stu-id="bee23-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![снимок экрана с увеличенным содержимым с инвертированными цветами](images/color-inversion.png)

<span data-ttu-id="bee23-243">Функция [**магсетколореффект**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) позволяет применять другие цветовые эффекты, устанавливая матрицу преобразования цветов, определяемую приложением.</span><span class="sxs-lookup"><span data-stu-id="bee23-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="bee23-244">Например, следующая функция задает матрицу преобразования цвета, которая преобразует цвета в градации серого.</span><span class="sxs-lookup"><span data-stu-id="bee23-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="bee23-245">Дополнительные сведения о работе преобразований цветов см. в разделе [Использование матрицы цветов для преобразования одного цвета](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) в документации GDI+.</span><span class="sxs-lookup"><span data-stu-id="bee23-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="bee23-246">Выборочное увеличение</span><span class="sxs-lookup"><span data-stu-id="bee23-246">Selective Magnification</span></span>

<span data-ttu-id="bee23-247">По умолчанию увеличение применяется ко всем окнам, Кроме окна лупы.</span><span class="sxs-lookup"><span data-stu-id="bee23-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="bee23-248">Чтобы указать, какие окна должны быть увеличены, вызовите функцию [**магсетвиндовфилтерлист**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) .</span><span class="sxs-lookup"><span data-stu-id="bee23-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="bee23-249">Этот метод принимает либо список окон для увеличения, либо список окон, которые необходимо исключить из увеличения.</span><span class="sxs-lookup"><span data-stu-id="bee23-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee23-250">См. также</span><span class="sxs-lookup"><span data-stu-id="bee23-250">Related topics</span></span>

[<span data-ttu-id="bee23-251">API увеличения</span><span class="sxs-lookup"><span data-stu-id="bee23-251">Magnification API</span></span>](entry-magapi-sdk.md)