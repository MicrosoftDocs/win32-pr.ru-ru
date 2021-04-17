---
title: Создание подключаемого модуля для Интернет-магазина типа 1
description: Создание подключаемого модуля для Интернет-магазина типа 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Интернет-магазины проигрывателя Windows Media, подключаемые модули
- Интернет-магазины, подключаемые модули
- Тип 1 Интернет-магазины, подключаемые модули
- Интернет-магазины проигрывателя Windows Media, создание подключаемых модулей
- Интернет-магазины, создание подключаемых модулей
- Тип 1 Интернет-магазины, создание подключаемых модулей
- Интернет-магазины проигрывателя Windows Media, интерфейс Ивмпконтентпартнер
- Интернет-магазины, интерфейс Ивмпконтентпартнер
- Тип 1 Интернет-магазины, интерфейс Ивмпконтентпартнер
- подключаемые модули, Интернет-магазины проигрывателя Windows Media
- подключаемые модули, Интернет-магазины
- подключаемые модули, тип 1 Интернет-магазины
- подключаемые модули, интерфейс Ивмпконтентпартнер
- подключаемые модули, сборка
- Подключаемые модули проигрывателя Windows Media, введите 1 Интернет-магазины
- Подключаемые модули проигрывателя Windows Media, Интернет-магазины
- Подключаемые модули проигрывателя Windows Media, Интернет-магазины проигрывателя Windows Media
- Подключаемые модули проигрывателя Windows Media, интерфейс Ивмпконтентпартнер
- Подключаемые модули проигрывателя Windows Media, сборка
- ивмпконтентпартнер
- Создание подключаемых модулей, тип 1 Интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691466"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a><span data-ttu-id="3368d-124">Создание подключаемого модуля для Интернет-магазина типа 1</span><span class="sxs-lookup"><span data-stu-id="3368d-124">Building the Plug-in for a Type 1 Online Store</span></span>

<span data-ttu-id="3368d-125">Интернет-магазин типа 1 должен предоставлять подключаемый модуль, реализующий интерфейс [**ивмпконтентпартнер**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="3368d-125">A type 1 online store must provide a plug-in that implements the [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="3368d-126">Подключаемый модуль запускается в отдельном процессе из проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3368d-126">The plug-in runs in a separate process from Windows Media Player.</span></span>

<span data-ttu-id="3368d-127">Ниже приведены шаги по созданию подключаемого модуля, запускаемого вне процесса.</span><span class="sxs-lookup"><span data-stu-id="3368d-127">The steps for creating a plug-in that runs out-of-process are as follows:</span></span>

1.  <span data-ttu-id="3368d-128">Создайте подключаемый модуль, как если бы он был внутрипроцессный COM-сервером.</span><span class="sxs-lookup"><span data-stu-id="3368d-128">Write your plug-in as if it were an in-process COM server.</span></span>
2.  <span data-ttu-id="3368d-129">Создайте запись реестра **дллсуррогате** на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="3368d-129">Create a **DllSurrogate** registry entry on the user's computer.</span></span> <span data-ttu-id="3368d-130">Запись **дллсуррогате** информирует среду выполнения com о том, что подключаемый модуль должен быть создан в экземпляре СУРРОГАТНОЙ библиотеки DLL по умолчанию, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="3368d-130">The **DllSurrogate** entry informs the COM runtime that your plug-in should be created in an instance of the default DLL surrogate, dllhost.exe.</span></span>

<span data-ttu-id="3368d-131">Подробные сведения о регистрации подключаемого модуля см. в разделе [разделы реестра и записи для Интернет-магазина типа 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="3368d-131">For detailed information about registering your plug-in, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="3368d-132">Для подключаемого модуля не нужно создавать прокси-сервер или код заглушки.</span><span class="sxs-lookup"><span data-stu-id="3368d-132">You do not need to create any proxy or stub code for your plug-in.</span></span> <span data-ttu-id="3368d-133">Вся поддержка упаковки обеспечивается проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3368d-133">All of the marshaling support is provided by Windows Media Player.</span></span>

<span data-ttu-id="3368d-134">Для быстрого создания подключаемого модуля, который служит отправной точкой, можно использовать мастер подключаемых модулей интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="3368d-134">You can use the online store plug-in wizard to quickly create a plug-in that serves as a starting point.</span></span> <span data-ttu-id="3368d-135">Дополнительные сведения см. в статье [Установка подключаемого модуля интернет-магазина](installing-the-online-store-plug-in-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="3368d-135">For more information, see [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3368d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="3368d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3368d-137">**Справка по программированию для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="3368d-137">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




