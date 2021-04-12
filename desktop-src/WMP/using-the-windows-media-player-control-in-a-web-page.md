---
title: Использование элемента управления проигрывателя Windows Media на веб-странице
description: Использование элемента управления проигрывателя Windows Media на веб-странице
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX, веб-страницы
- внедрение, веб-страницы
- Внедрение веб-страниц, о программе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258713"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="79394-115">Использование элемента управления проигрывателя Windows Media на веб-странице</span><span class="sxs-lookup"><span data-stu-id="79394-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="79394-116">Внедрение элемента управления проигрывателя Windows Media на веб-страницу позволяет полностью настроить способ взаимодействия пользователя с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="79394-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="79394-117">Вы можете использовать интерфейс, предоставляемый элементом управления, или скрыть его и отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="79394-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="79394-118">Можно указать несколько свойств элемента управления проигрывателя Windows Media в точке встраивания элемента управления или задать свойства проигрывателя и вызвать методы проигрывателя в коде скрипта.</span><span class="sxs-lookup"><span data-stu-id="79394-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="79394-119">В следующих разделах описаны основные принципы внедрения элемента управления на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="79394-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="79394-120">Section</span><span class="sxs-lookup"><span data-stu-id="79394-120">Section</span></span>                                                                                                        | <span data-ttu-id="79394-121">Описание</span><span class="sxs-lookup"><span data-stu-id="79394-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79394-122">Скрытие элемента управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="79394-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="79394-123">Описывает параметры для скрытия элемента управления проигрывателя Windows Media, когда требуется предоставить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="79394-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="79394-124">Элементы PARAM в элементе OBJECT</span><span class="sxs-lookup"><span data-stu-id="79394-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="79394-125">Описание инициализации элемента управления проигрывателя Windows Media при его внедрении.</span><span class="sxs-lookup"><span data-stu-id="79394-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="79394-126">Простой пример создания сценариев на веб-странице</span><span class="sxs-lookup"><span data-stu-id="79394-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="79394-127">Описывает простой, но полный пример встроенного элемента управления "проигрыватель" с настраиваемым пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="79394-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="79394-128">Использование элемента управления проигрывателя Windows Media с браузером Firefox</span><span class="sxs-lookup"><span data-stu-id="79394-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="79394-129">Описание внедрения элемента управления проигрывателя Windows Media в веб-страницу для правильного отображения в браузере Firefox.</span><span class="sxs-lookup"><span data-stu-id="79394-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="79394-130">Использование проигрывателя Windows Media с Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="79394-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="79394-131">Описывает использование элемента управления проигрывателя Windows Media с Netscape 7,1 и другими веб-браузерами на основе Gecko.</span><span class="sxs-lookup"><span data-stu-id="79394-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="79394-132">Мобильный элемент управления Windows Media Player 10 содержит функциональные возможности, основанные на подмножестве функциональных возможностей, предоставляемых в классической версии элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79394-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="79394-133">Таким образом, его можно внедрить в веб-страницу Pocket Internet Explorer таким же образом, как и элемент управления Desktop на веб-странице Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="79394-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="79394-134">Чтобы узнать, поддерживается ли конкретный метод, свойство или событие для мобильного элемента управления Windows Media Player 10, см. раздел [Справочник по объектной модели для создания сценариев](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="79394-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="79394-135">См. также</span><span class="sxs-lookup"><span data-stu-id="79394-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79394-136">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="79394-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




