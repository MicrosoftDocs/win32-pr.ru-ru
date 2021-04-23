---
title: Компиляция примера проекта
description: Компиляция примера проекта
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Интернет-магазины проигрывателя Windows Media, компиляция образцов проектов
- Интернет-магазины, компиляция образцов проектов
- Тип 2 Интернет-магазинов, компиляция образцов проектов
- Интернет-магазины проигрывателя Windows Media, примеры проектов
- Интернет-магазины, примеры проектов
- Тип 2 Интернет-магазинов, примеры проектов
- Интернет-магазины проигрывателя Windows Media, мастер проектов
- Интернет-магазины, мастер проектов
- Тип 2 Интернет-магазинов, мастер проектов
- подключаемые модули, мастер проектов
- Подключаемые модули проигрывателя Windows Media, мастер проектов
- Компиляция образцов проектов
- Примеры, тип 2 Интернет-магазинов
- Мастер проектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691275"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="0cc39-117">Компиляция примера проекта</span><span class="sxs-lookup"><span data-stu-id="0cc39-117">Compiling the Sample Project</span></span>

<span data-ttu-id="0cc39-118">Мастер создает все файлы, необходимые для компиляции примера проекта, поэтому вам не нужно изменять параметры проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cc39-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="0cc39-119">В Visual Studio в меню **Сборка** выберите пункт **построить решение** , чтобы создать и зарегистрировать COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="0cc39-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="0cc39-120">По умолчанию конфигурация отладки активна.</span><span class="sxs-lookup"><span data-stu-id="0cc39-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="0cc39-121">В Windows Vista и более поздних версиях проект не будет успешно построен, если вы не запустите Visual Studio с полным маркером доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="0cc39-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="0cc39-122">Щелкните правой кнопкой мыши имя или значок Visual Studio и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="0cc39-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="0cc39-123">Прежде чем пытаться выполнить сборку проекта, необходимо настроить среду разработки так, чтобы она указывала на папки с именами include и lib, где установлен Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0cc39-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="0cc39-124">Компилятору и компоновщику потребуется доступ к некоторым файлам в этих папках.</span><span class="sxs-lookup"><span data-stu-id="0cc39-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="0cc39-125">Если вы запустили программу регистрации Visual Studio, которая поставляется вместе с Windows Vista SDK, возможно, среда разработки уже настроена так, чтобы она указывала на Windows SDK папки include и lib.</span><span class="sxs-lookup"><span data-stu-id="0cc39-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="0cc39-126">В противном случае необходимо вручную настроить среду разработки.</span><span class="sxs-lookup"><span data-stu-id="0cc39-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="0cc39-127">Чтобы вручную настроить Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0cc39-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="0cc39-128">В меню **Сервис** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="0cc39-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="0cc39-129">Щелкните **проекты и решения**, а затем выберите **каталоги VC + +**.</span><span class="sxs-lookup"><span data-stu-id="0cc39-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="0cc39-130">В разделе **Показ каталогов для** выберите **включить файлы** или **файлы библиотек**.</span><span class="sxs-lookup"><span data-stu-id="0cc39-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="0cc39-131">Добавьте каталоги для необходимых файлов.</span><span class="sxs-lookup"><span data-stu-id="0cc39-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cc39-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0cc39-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cc39-133">Создание подключаемого модуля для Интернет-магазина типа 2</span><span class="sxs-lookup"><span data-stu-id="0cc39-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




