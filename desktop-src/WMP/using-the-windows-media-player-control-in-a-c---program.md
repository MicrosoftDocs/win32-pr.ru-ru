---
title: Использование элемента управления проигрывателя Windows Media в программе на языке C++
description: Использование элемента управления проигрывателя Windows Media в программе на языке C++
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258714"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="1dd2b-119">Использование элемента управления проигрывателя Windows Media в программе на языке C++</span><span class="sxs-lookup"><span data-stu-id="1dd2b-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="1dd2b-120">Использование C++ для внедрения элемента управления проигрывателя Windows Media поддерживается для Windows Media Player 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="1dd2b-121">Существует несколько различных способов использования элемента управления проигрывателя Windows Media в программе C++.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="1dd2b-122">Можно создать экземпляр элемента управления в консольном приложении или встроить элемент управления в приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="1dd2b-123">Кроме того, можно реализовать интерфейсы, позволяющие запускать внедренный элемент управления Player в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="1dd2b-124">Пользовательский интерфейс внедренного элемента управления можно настроить, применив файл определения обложки.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="1dd2b-125">Эти сведения описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="1dd2b-126">Раздел</span><span class="sxs-lookup"><span data-stu-id="1dd2b-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="1dd2b-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1dd2b-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dd2b-128">Использование элемента управления проигрывателя Windows Media в консольном приложении</span><span class="sxs-lookup"><span data-stu-id="1dd2b-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="1dd2b-129">Описывает простое консольное приложение C++, которое создает экземпляр элемента управления проигрывателя Windows Media для вывода версии.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="1dd2b-130">Размещение элемента управления проигрывателя Windows Media в приложении Windows</span><span class="sxs-lookup"><span data-stu-id="1dd2b-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="1dd2b-131">Описывает использование окна узла ATL ActiveX для внедрения элемента управления проигрывателя Windows Media в программу Windows.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="1dd2b-132">Реализация удаленного управления проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="1dd2b-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="1dd2b-133">Описывает внедрение элемента управления проигрывателя Windows Media в программу C++ в удаленном режиме, что позволяет пользователям откреплять элемент управления для переключения в полноэкранный режим проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="1dd2b-134">Обработка событий в C++</span><span class="sxs-lookup"><span data-stu-id="1dd2b-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="1dd2b-135">Описывает, как получать уведомления о событиях из проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="1dd2b-136">Использование обложек с элементом управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="1dd2b-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="1dd2b-137">Описывает применение файла обложки к элементу управления проигрывателя Windows Media, внедренному в программу C++.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="1dd2b-138">Вы можете внедрить мобильный элемент управления Windows Media Player 10 в Windows CEое приложение.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="1dd2b-139">Методы, используемые для этого, похожи на те, которые используются для настольного элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="1dd2b-140">Однако существуют различия между ATL для Windows и ATL для Windows CE.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="1dd2b-141">В этой документации описаны различия между этими реализациями, где это уместно.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1dd2b-142">См. также</span><span class="sxs-lookup"><span data-stu-id="1dd2b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dd2b-143">**Справочник по объектной модели для C++**</span><span class="sxs-lookup"><span data-stu-id="1dd2b-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="1dd2b-144">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="1dd2b-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




