---
title: Создание примера проекта
description: Создание примера проекта
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Интернет-магазины проигрывателя Windows Media, создание образцов проектов
- Интернет-магазины, создание образцов проектов
- Тип 2 Интернет-магазинов, создание образцов проектов
- Интернет-магазины проигрывателя Windows Media, примеры проектов
- Интернет-магазины, примеры проектов
- Тип 2 Интернет-магазинов, примеры проектов
- Интернет-магазины проигрывателя Windows Media, мастер проектов
- Интернет-магазины, мастер проектов
- Тип 2 Интернет-магазинов, мастер проектов
- подключаемые модули, мастер проектов
- Подключаемые модули проигрывателя Windows Media, мастер проектов
- Создание образцов проектов
- Примеры, тип 2 Интернет-магазинов
- Мастер проектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104133559"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="3d39c-117">Создание примера проекта</span><span class="sxs-lookup"><span data-stu-id="3d39c-117">Creating a Sample Project</span></span>

<span data-ttu-id="3d39c-118">Чтобы создать новый проект с помощью мастера проектов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3d39c-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="3d39c-119">Откройте среду Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3d39c-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="3d39c-120">В меню **Файл** выберите пункт **Создать**, а затем команду **Проект**.</span><span class="sxs-lookup"><span data-stu-id="3d39c-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="3d39c-121">В списке **типы проектов** выберите **Visual C++ проекты**.</span><span class="sxs-lookup"><span data-stu-id="3d39c-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="3d39c-122">В списке **шаблоны** выберите **Мастер Интернет-магазинов проигрывателя Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="3d39c-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="3d39c-123">Введите имя и расположение проекта.</span><span class="sxs-lookup"><span data-stu-id="3d39c-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="3d39c-124">Нажмите кнопку **ОК** , чтобы запустить мастер проектов.</span><span class="sxs-lookup"><span data-stu-id="3d39c-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="3d39c-125">Выберите **тип 2 (интеграция с базовой интеграцией)** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3d39c-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="3d39c-126">Введите понятное имя и идентификатор распространителя содержимого для службы.</span><span class="sxs-lookup"><span data-stu-id="3d39c-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="3d39c-127">Введите URL-адрес веб-страницы, которая удаляет службу с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d39c-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="3d39c-128">Значение, которое вы задают для идентификатора распространителя содержимого, не должно содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="3d39c-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="3d39c-129">Мастер удаляет все пробелы из предоставленной строки.</span><span class="sxs-lookup"><span data-stu-id="3d39c-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="3d39c-130">Нажмите кнопку **Готово**, чтобы создать проект.</span><span class="sxs-lookup"><span data-stu-id="3d39c-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="3d39c-131">Мастер автоматически создает новый проект C++, который создает подключаемый модуль магазина типа 2, реализующий интерфейсы **ивмпсубскриптионсервице** и **IWMPSubscriptionService2** .</span><span class="sxs-lookup"><span data-stu-id="3d39c-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="3d39c-132">Каждый раз при запуске мастера создается тот же проект, но компонент, создаваемый при компиляции проекта, имеет уникальный идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="3d39c-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="3d39c-133">Имя проекта, понятное имя и идентификатор распространителя содержимого могут также отличаться в зависимости от значений, указанных при запуске мастера.</span><span class="sxs-lookup"><span data-stu-id="3d39c-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="3d39c-134">Пример проекта регистрирует компонент, используя имя ключа, которое соответствует значению, указанному для понятного имени.</span><span class="sxs-lookup"><span data-stu-id="3d39c-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="3d39c-135">В примере используется код библиотеки активных шаблонов (ATL) для реализации COM-реализаций.</span><span class="sxs-lookup"><span data-stu-id="3d39c-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="3d39c-136">Мастер создает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="3d39c-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="3d39c-137">*Имя_проекта* DLL. cpp.</span><span class="sxs-lookup"><span data-stu-id="3d39c-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="3d39c-138">Реализует экспорт библиотеки динамической компоновки (DLL), например основную функцию точки входа библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3d39c-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="3d39c-139">Также содержит декларацию объектов ATL и объявление модуля.</span><span class="sxs-lookup"><span data-stu-id="3d39c-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="3d39c-140">*Имя_проекта*. cpp.</span><span class="sxs-lookup"><span data-stu-id="3d39c-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="3d39c-141">Содержит реализации по умолчанию для методов интерфейсов Ивмпсубскриптионсервице и IWMPSubscriptionService2.</span><span class="sxs-lookup"><span data-stu-id="3d39c-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="3d39c-142">Также содержит код для определения диалоговых окон, которые открывается при вызове метода проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3d39c-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="3d39c-143">*Имя_проекта*. def. Объявляет экспорты DLL.</span><span class="sxs-lookup"><span data-stu-id="3d39c-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="3d39c-144">StdAfx. cpp.</span><span class="sxs-lookup"><span data-stu-id="3d39c-144">StdAfx.cpp.</span></span> <span data-ttu-id="3d39c-145">Включает стандартные заголовки.</span><span class="sxs-lookup"><span data-stu-id="3d39c-145">Includes standard headers.</span></span>
-   <span data-ttu-id="3d39c-146">WMP. h.</span><span class="sxs-lookup"><span data-stu-id="3d39c-146">wmp.h.</span></span> <span data-ttu-id="3d39c-147">Файл заголовка проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3d39c-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="3d39c-148">вмпплуг. h.</span><span class="sxs-lookup"><span data-stu-id="3d39c-148">wmpplug.h.</span></span> <span data-ttu-id="3d39c-149">Файл заголовка подключаемого модуля проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3d39c-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="3d39c-150">субскриптионсервицес. h.</span><span class="sxs-lookup"><span data-stu-id="3d39c-150">subscriptionservices.h.</span></span> <span data-ttu-id="3d39c-151">Файл заголовка Windows Media Player в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3d39c-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="3d39c-152">Resource. h.</span><span class="sxs-lookup"><span data-stu-id="3d39c-152">resource.h.</span></span> <span data-ttu-id="3d39c-153">Содержит определения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d39c-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="3d39c-154">**Имя_проекта**. h.</span><span class="sxs-lookup"><span data-stu-id="3d39c-154">**ProjectName**.h.</span></span> <span data-ttu-id="3d39c-155">Содержит определения классов для объекта Интернет-магазина и диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="3d39c-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="3d39c-156">Определяет идентификатор класса объекта и константу идентификатора распространителя содержимого.</span><span class="sxs-lookup"><span data-stu-id="3d39c-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="3d39c-157">Файл StdAfx. h.</span><span class="sxs-lookup"><span data-stu-id="3d39c-157">StdAfx.h.</span></span> <span data-ttu-id="3d39c-158">Содержит стандартные системные включения.</span><span class="sxs-lookup"><span data-stu-id="3d39c-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="3d39c-159">*Имя_проекта*. rc.</span><span class="sxs-lookup"><span data-stu-id="3d39c-159">*ProjectName*.rc.</span></span> <span data-ttu-id="3d39c-160">Файл описания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d39c-160">The resource script file.</span></span> <span data-ttu-id="3d39c-161">Это содержит определения для ресурсов диалоговых окон и элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3d39c-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="3d39c-162">Здесь также хранится таблица строк.</span><span class="sxs-lookup"><span data-stu-id="3d39c-162">This is also where the string table is stored.</span></span> <span data-ttu-id="3d39c-163">Таблица строк содержит имя проекта и строковые константы с понятными именами.</span><span class="sxs-lookup"><span data-stu-id="3d39c-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="3d39c-164">Обычно этот файл работает в редакторе ресурсов Visual Studio, а не в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="3d39c-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="3d39c-165">*Имя_проекта*. RGS.</span><span class="sxs-lookup"><span data-stu-id="3d39c-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="3d39c-166">Файл скрипта реестра.</span><span class="sxs-lookup"><span data-stu-id="3d39c-166">The registry script file.</span></span> <span data-ttu-id="3d39c-167">Этот файл содержит сведения, используемые для добавления класса компонента в реестр, чтобы проигрыватель Windows Media мог его разместить.</span><span class="sxs-lookup"><span data-stu-id="3d39c-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="3d39c-168">Имя ключа для службы можно изменить в этом файле.</span><span class="sxs-lookup"><span data-stu-id="3d39c-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="3d39c-169">Необходимо задать базовый адрес для библиотеки DLL 0x0F100000 во избежание конфликтов с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3d39c-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d39c-170">См. также</span><span class="sxs-lookup"><span data-stu-id="3d39c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d39c-171">**Создание подключаемого модуля для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="3d39c-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="3d39c-172">**Интерфейс Ивмпсубскриптионсервице**</span><span class="sxs-lookup"><span data-stu-id="3d39c-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="3d39c-173">**Интерфейс IWMPSubscriptionService2**</span><span class="sxs-lookup"><span data-stu-id="3d39c-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




