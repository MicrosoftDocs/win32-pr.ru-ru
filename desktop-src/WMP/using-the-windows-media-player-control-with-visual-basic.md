---
title: Использование элемента управления проигрывателя Windows Media с Visual Basic
description: Использование элемента управления проигрывателя Windows Media с Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media Visual Basic
- Объектная модель проигрывателя Windows Media, Visual Basic
- Объектная модель, Visual Basic
- Проигрыватель Windows Media Mobile, Visual Basic
- Элемент управления ActiveX проигрывателя Windows Media, Visual Basic
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media Visual Basic
- Элемент управления ActiveX, Visual Basic
- Внедрение программ на основе Visual Basic
- внедрение, программы на основе Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330835"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="adc1a-119">Использование элемента управления проигрывателя Windows Media с Visual Basic</span><span class="sxs-lookup"><span data-stu-id="adc1a-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="adc1a-120">В этом разделе описывается, как использовать Windows Media Player 9 Series или более поздней версии элемента управления ActiveX в приложениях, созданных с помощью Microsoft Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="adc1a-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="adc1a-121">Приступая к работе</span><span class="sxs-lookup"><span data-stu-id="adc1a-121">Getting Started</span></span>

<span data-ttu-id="adc1a-122">Чтобы добавить элемент управления проигрывателя Windows Media на панель элементов, сначала выберите **компоненты** в меню **проект** .</span><span class="sxs-lookup"><span data-stu-id="adc1a-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="adc1a-123">В диалоговом окне Компоненты установите флажок рядом с полем "проигрыватель Windows Media".</span><span class="sxs-lookup"><span data-stu-id="adc1a-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="adc1a-124">В нижней части диалогового окна убедитесь, что выбранный файл имеет wmp.dll.</span><span class="sxs-lookup"><span data-stu-id="adc1a-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="adc1a-125">После закрытия диалогового окна экземпляр элемента управления проигрывателя Windows Media можно поместить в форму обычным образом.</span><span class="sxs-lookup"><span data-stu-id="adc1a-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="adc1a-126">Вы можете задать множество свойств управления с помощью окно свойств.</span><span class="sxs-lookup"><span data-stu-id="adc1a-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="adc1a-127">Чтобы задать некоторые свойства, необходимо использовать диалоговое окно Свойства проигрывателя Windows Media, которое открывается с помощью элемента "(пользовательский)" в окно свойств.</span><span class="sxs-lookup"><span data-stu-id="adc1a-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="adc1a-128">Ссылки на объекты</span><span class="sxs-lookup"><span data-stu-id="adc1a-128">Object References</span></span>

<span data-ttu-id="adc1a-129">Для получения ссылок на определенные объекты используются определенные свойства управления проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="adc1a-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="adc1a-130">Например, свойство **кдромколлектион** возвращает ссылку на объект **кдромколлектион** .</span><span class="sxs-lookup"><span data-stu-id="adc1a-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="adc1a-131">Такую ссылку необходимо назначить переменной, объявленной в качестве соответствующего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="adc1a-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="adc1a-132">Например, при использовании свойства **кдромколлектион** его возвращаемое значение присваивается переменной типа **ивмпкдромколлектион**.</span><span class="sxs-lookup"><span data-stu-id="adc1a-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="adc1a-133">Ознакомьтесь с разделом [интерфейсы](interfaces.md) в [справочнике по объектной модели для C++](object-model-reference-for-c.md) , чтобы узнать, какие объекты реализуют несколько интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="adc1a-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="adc1a-134">В таких случаях необходимо объявить объектную переменную в качестве самого высокого номера интерфейса, описанного в этом пакете SDK, чтобы получить доступ ко всем свойствам и методам этого объекта.</span><span class="sxs-lookup"><span data-stu-id="adc1a-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="adc1a-135">Например, следует присвоить значение свойства **куррентмедиа** элемента управления проигрывателя Windows Media переменной, объявленной как **IWMPMedia3** , чтобы гарантировать доступ к методам **жетаттрибутекаунтбитипе** и **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="adc1a-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="adc1a-136">Объект **виндовсмедиаплайер** реализует все свойства и методы интерфейсов **ивмпкоре**, **IWMPCore2**, **IWMPCore3**, **ивмпплайер**, **IWMPPlayer2**, **IWMPPlayer3** и **IWMPPlayer4** .</span><span class="sxs-lookup"><span data-stu-id="adc1a-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="adc1a-137">Для этих интерфейсов не нужно объявлять отдельные переменные.</span><span class="sxs-lookup"><span data-stu-id="adc1a-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="adc1a-138">Доступ ко всем членам можно получить с помощью имени, назначенного экземпляру **виндовсмедиаплайер** .</span><span class="sxs-lookup"><span data-stu-id="adc1a-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="adc1a-139">В обозревателе объектов Visual Basic вы увидите множество интерфейсов, предназначенных для частного использования элементом управления проигрывателя Windows Media, включая некоторые, которые поддерживаются разработчиками обложки.</span><span class="sxs-lookup"><span data-stu-id="adc1a-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="adc1a-140">Следует использовать только объекты, свойства, методы и события, описанные в этом пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="adc1a-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="adc1a-141">Дополнительные советы</span><span class="sxs-lookup"><span data-stu-id="adc1a-141">Additional Tips</span></span>

-   <span data-ttu-id="adc1a-142">В справочной документации показан синтаксис JScript.</span><span class="sxs-lookup"><span data-stu-id="adc1a-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="adc1a-143">В JScript аргументы, передаваемые методам, всегда заключаются в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="adc1a-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="adc1a-144">В Visual Basic 6,0 аргументы, передаваемые методам, не возвращающим значение, не должны заключаться в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="adc1a-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="adc1a-145">Некоторые свойства или методы могут не отображаться в функции автосписковое автозавершение кода в Visual Basic редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="adc1a-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="adc1a-146">Вы по-прежнему можете использовать эти члены, вводя их имена точно так же, как они отображаются в этой документации.</span><span class="sxs-lookup"><span data-stu-id="adc1a-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="adc1a-147">Управление внешним видом элемента управления с помощью свойства **UIMODE** .</span><span class="sxs-lookup"><span data-stu-id="adc1a-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="adc1a-148">Это можно сделать двумя способами.</span><span class="sxs-lookup"><span data-stu-id="adc1a-148">You can do so in two ways.</span></span> <span data-ttu-id="adc1a-149">Можно использовать раскрывающийся список **выбрать режим** в диалоговом окне Свойства проигрывателя Windows Media или ввести правильное значение в окно свойств.</span><span class="sxs-lookup"><span data-stu-id="adc1a-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="adc1a-150">В частности, не используйте свойство **Visible** для скрытия элемента управления. Вместо этого присвойте свойству **UIMODE** значение «невидимый».</span><span class="sxs-lookup"><span data-stu-id="adc1a-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adc1a-151">См. также</span><span class="sxs-lookup"><span data-stu-id="adc1a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adc1a-152">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="adc1a-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




