---
title: Использование обложек с элементом управления проигрывателя Windows Media
description: Использование обложек с элементом управления проигрывателя Windows Media
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, C++
- Объектная модель проигрывателя Windows Media, C++
- Объектная модель, C++
- Проигрыватель Windows Media Mobile, C++
- Элемент управления ActiveX проигрывателя Windows Media, C++
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, C++
- Элемент управления ActiveX, C++
- Внедрение программ на C++
- внедрение, программы на C++
- Элемент управления ActiveX проигрывателя Windows Media, обложки
- Элемент управления ActiveX проигрывателя Windows Media для мобильных устройств, обложки
- Элемент управления ActiveX, обложки
- обложки, встраивание элемента управления ActiveX
- Обложки проигрывателя Windows Media, встраивание элемента управления ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253310"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="83d0d-124">Использование обложек с элементом управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="83d0d-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="83d0d-125">При внедрении элемента управления проигрывателя Windows Media в программу на языке C++ можно настроить пользовательский интерфейс проигрывателя, применив к нему файл определения обложки.</span><span class="sxs-lookup"><span data-stu-id="83d0d-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="83d0d-126">Файл определения обложки — это документ на основе XML, указывающий расположение стандартных и настраиваемых компонентов пользовательского интерфейса, а также любую сопроводительную графику.</span><span class="sxs-lookup"><span data-stu-id="83d0d-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="83d0d-127">С помощью Microsoft JScript можно указать поведение этих компонентов и управлять проигрывателем Windows Media Player без дополнительной нагрузки на C++ и синтаксиса COM.</span><span class="sxs-lookup"><span data-stu-id="83d0d-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="83d0d-128">Обложки предоставляют простой способ, позволяющий разделять код пользовательского интерфейса и код основной программы, чтобы их можно было обслуживать и разрабатывать независимо.</span><span class="sxs-lookup"><span data-stu-id="83d0d-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="83d0d-129">Можно также повторно использовать обложки, изначально разработанные для использования автономным проигрывателем в режиме обложки.</span><span class="sxs-lookup"><span data-stu-id="83d0d-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="83d0d-130">Код обложки, разработанный специально для программ на C++, может взаимодействовать с программами через объект, предоставляемый программой.</span><span class="sxs-lookup"><span data-stu-id="83d0d-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="83d0d-131">Чтобы включить режим обложки для элемента управления проигрывателя Windows Media, программа должна реализовать интерфейс **ивмпремотемедиасервицес** .</span><span class="sxs-lookup"><span data-stu-id="83d0d-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="83d0d-132">Хотя обложки можно использовать вместе с элементом управления и одновременно с удаленным элементом управления, этот интерфейс можно использовать для включения любой из компонентов без включения другого.</span><span class="sxs-lookup"><span data-stu-id="83d0d-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="83d0d-133">Чтобы отключить удаленное взаимодействие, просто передайте значение Local в качестве параметра out метода **жетсервицетипе** и возвратите HRESULT из E \_ Нотимпл из метода **имя_приложения** .</span><span class="sxs-lookup"><span data-stu-id="83d0d-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="83d0d-134">Чтобы переключить элемент управления проигрывателя Windows Media в режим обложки, вызовите метод **ивмпплайер::p UT \_ uiMode** , передав значение Custom.</span><span class="sxs-lookup"><span data-stu-id="83d0d-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="83d0d-135">Укажите путь и имя файла определения обложки для использования, возвращая его из метода **ивмпремотемедиасервицес:: жеткустомуимоде** .</span><span class="sxs-lookup"><span data-stu-id="83d0d-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="83d0d-136">Если вы хотите предоставить объект, поддерживающий скрипт, для обмена данными между обложкой и программой, передайте имя и указатель на указатель **IDispatch** в качестве двух параметров out метода **Ивмпремотемедиасервицес:: жетскриптаблеобжект** .</span><span class="sxs-lookup"><span data-stu-id="83d0d-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="83d0d-137">Затем Ваша Обложка может вызывать объект, поддерживающий скрипт, используя имя, указанное как глобальный атрибут, аналогичный глобальному атрибуту **Player** .</span><span class="sxs-lookup"><span data-stu-id="83d0d-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="83d0d-138">Обложка, применяемая к удаленному элементу управления проигрывателя Windows Media, может получить доступ к объекту **плайераппликатион** , используя другой глобальный атрибут с именем **плайераппликатион**.</span><span class="sxs-lookup"><span data-stu-id="83d0d-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="83d0d-139">Поскольку свойства **Player. плайераппликатион** недоступны для обложек, необходимо использовать этот глобальный атрибут, если код обложки должен управлять закреплением и отстыковкой.</span><span class="sxs-lookup"><span data-stu-id="83d0d-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="83d0d-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="83d0d-140">Samples</span></span>

<span data-ttu-id="83d0d-141">Пакет установки пакета SDK для проигрывателя Windows Media устанавливает пример, демонстрирующий применение обложки к элементу управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83d0d-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="83d0d-142">Дополнительные сведения см. в примере Ремотескин.</span><span class="sxs-lookup"><span data-stu-id="83d0d-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83d0d-143">См. также</span><span class="sxs-lookup"><span data-stu-id="83d0d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83d0d-144">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="83d0d-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="83d0d-145">**Использование элемента управления проигрывателя Windows Media в программе на языке C++**</span><span class="sxs-lookup"><span data-stu-id="83d0d-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




