---
title: Внедрение элемента управления проигрывателя Windows Media в пользовательскую программу
description: Внедрение элемента управления проигрывателя Windows Media в пользовательскую программу
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- внедрение, пользовательские программы
- пользовательское внедрение программы
- внедрение, программы на основе Visual Basic
- Внедрение программ на основе Visual Basic
- внедрение, использование методов COM вручную
- Ручное внедрение с помощью методов COM
- внедрение, программы на C++
- Внедрение программ на C++
- внедрение, программы Visual Studio
- Visual Studio, внедрение программ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067750"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="02698-120">Внедрение элемента управления проигрывателя Windows Media в пользовательскую программу</span><span class="sxs-lookup"><span data-stu-id="02698-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="02698-121">Поскольку элемент управления ActiveX проигрывателя Windows Media основан на технологии модели COM, его можно внедрить в программы, написанные на множестве языков программирования.</span><span class="sxs-lookup"><span data-stu-id="02698-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="02698-122">Элемент управления проигрывателя Windows Media представляет собой простой способ добавления сложных функций цифрового мультимедиа в любую программу.</span><span class="sxs-lookup"><span data-stu-id="02698-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="02698-123">В Microsoft Visual Basic можно добавить элемент управления на панель элементов «элементы управления», поместить его в форму и настроить свойства элемента управления в окне «Свойства».</span><span class="sxs-lookup"><span data-stu-id="02698-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="02698-124">Если вам нужен настраиваемый пользовательский интерфейс, можно поместить кнопки команд в форму и добавить код, управляющий элементом управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02698-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="02698-125">Внедрение элемента управления в программу на основе Visual Basic очень похоже на его внедрение в документ Office и программирование с помощью VBA.</span><span class="sxs-lookup"><span data-stu-id="02698-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="02698-126">Кроме того, элемент управления можно внедрить вручную с помощью методов COM, чтобы создать экземпляр элемента управления и получить доступ к интерфейсам COM, задокументированным в [справочнике по объектной модели для C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="02698-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="02698-127">При внедрении элемента управления проигрывателя Windows Media в программу на языке C++ можно реализовать COM-интерфейсы, позволяющие элементу управления работать в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="02698-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="02698-128">Это означает, что внедренный элемент управления использует тот же механизм воспроизведения, что и полный режим проигрывателя, и пользователи могут переключаться между полным и закрепленным состоянием без прерывания воспроизведения цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="02698-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="02698-129">Вы также можете управлять отображением на различных панелях проигрывателя полноэкранного режима, когда пользователи переключаются в незакрепленное состояние.</span><span class="sxs-lookup"><span data-stu-id="02698-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="02698-130">При внедрении C++ также можно применить файл определения обложки к внедренному элементу управления Player.</span><span class="sxs-lookup"><span data-stu-id="02698-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="02698-131">Это простой способ создания упрощенного кода пользовательского интерфейса, который можно поддерживать отдельно от основного кода программы.</span><span class="sxs-lookup"><span data-stu-id="02698-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="02698-132">Microsoft Visual Studio поддерживает внедрение элементов управления ActiveX, включая элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02698-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="02698-133">При выборе этого действия Visual Studio создает новую альтернативную сборку взаимодействия (Interop) для управления взаимодействием между платформа .NET Framework и элементом управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02698-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="02698-134">Visual Studio использует средство платформа .NET Framework tlbimp.exe для создания сборки взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="02698-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="02698-135">Это означает, что подписи, отображаемые при использовании функции IntelliSense в Visual Studio, используют семантику, определенную текущей версией программы Tlbimp.</span><span class="sxs-lookup"><span data-stu-id="02698-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02698-136">См. также</span><span class="sxs-lookup"><span data-stu-id="02698-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02698-137">**Внедрение элемента управления проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="02698-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="02698-138">**Использование элемента управления проигрывателя Windows Media в программе на языке C++**</span><span class="sxs-lookup"><span data-stu-id="02698-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="02698-139">**Использование элемента управления проигрывателя Windows Media в платформа .NET Framework решении**</span><span class="sxs-lookup"><span data-stu-id="02698-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="02698-140">**Использование элемента управления проигрывателя Windows Media с Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="02698-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




