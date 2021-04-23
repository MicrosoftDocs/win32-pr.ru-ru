---
title: Внедрение элемента управления проигрывателя Windows Media в документ Office
description: Внедрение элемента управления проигрывателя Windows Media в документ Office
ms.assetid: 6d3466fb-a39d-4ebc-b439-a1a22d9d0800
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- внедрение, документы Office
- Внедрение документов Office
- внедрение, документы Word
- Внедрение документа Word
- внедрение, электронные таблицы Excel
- Внедрение электронных таблиц Excel
- внедрение, показ слайдов PowerPoint
- Внедрение показа слайдов PowerPoint
- внедрение, страницы FrontPage
- Внедрение страницы в FrontPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735781f6924b55bf0dff157fe14891068b052567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772803"
---
# <a name="embedding-the-windows-media-player-control-in-an-office-document"></a><span data-ttu-id="e7a9e-120">Внедрение элемента управления проигрывателя Windows Media в документ Office</span><span class="sxs-lookup"><span data-stu-id="e7a9e-120">Embedding the Windows Media Player Control in an Office Document</span></span>

<span data-ttu-id="e7a9e-121">Внедрение элемента управления проигрывателя Windows Media в документ Office — это простой способ добавить динамическое интерактивное мультимедийное содержимое в статичный статический документ.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-121">Embedding the Windows Media Player control in an Office document is an easy way to add dynamic, interactive digital media content to an otherwise static document.</span></span> <span data-ttu-id="e7a9e-122">Например, можно создать электронную таблицу в Microsoft Excel и вставить в нее видео с текстом «разговор», а также создать документ Microsoft Word и вставить короткий эффект анимации, иллюстрирующий точку, сделанную в тексте.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-122">For example, you can create a spreadsheet in Microsoft Excel and insert a "talking head" video summarizing a report, or you can create a Microsoft Word document and insert a short animation illustrating a point made in the text.</span></span> <span data-ttu-id="e7a9e-123">Если вам не нравится пользовательский интерфейс, предоставляемый элементом управления, можно использовать Microsoft Visual Basic для приложений (VBA) для создания пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-123">If you don't like the user interface provided by the control, you can use Microsoft Visual Basic for Applications (VBA) to provide a custom user interface.</span></span>

<span data-ttu-id="e7a9e-124">Внедрение элемента управления проигрывателя Windows Media в Microsoft PowerPoint® слайд-шоу позволяет дополнить динамические эффекты, уже предоставляемые этой программой.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-124">Embedding the Windows Media Player control in a Microsoft PowerPoint® slide show lets you supplement the dynamic effects already provided by that program.</span></span> <span data-ttu-id="e7a9e-125">При сохранении презентации в виде веб-страницы элемент управления проигрывателя Windows Media внедряется в HTML, как описано в статье [использование элемента управления проигрывателем Windows Media на странице](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="e7a9e-125">When you save the presentation as a webpage, the Windows Media Player control is embedded in the HTML as described in [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span> <span data-ttu-id="e7a9e-126">Это позволяет добавить дополнительный код скрипта, разработанный для других веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-126">This lets you add additional script code that you may have developed for other webpages.</span></span>

<span data-ttu-id="e7a9e-127">Другой способ легко создать веб-страницы, которые внедряют элемент управления проигрывателя Windows Media, — это® Microsoft FrontPage.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-127">Another way to easily generate webpages that embed the Windows Media Player control is with Microsoft FrontPage®.</span></span> <span data-ttu-id="e7a9e-128">FrontPage позволяет быстро создать страницу, добавить элемент управления проигрывателя Windows Media из меню и настроить его в диалоговом окне Свойства.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-128">FrontPage lets you rapidly create a page, add the Windows Media Player control from a menu, and configure it in a properties dialog box.</span></span> <span data-ttu-id="e7a9e-129">Опять же, в результате код HTML внедряет элемент управления проигрывателя Windows Media, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="e7a9e-129">Again, the resulting HTML embeds the Windows Media Player control just as described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7a9e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e7a9e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7a9e-131">**Внедрение элемента управления проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e7a9e-131">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="e7a9e-132">**Использование элемента управления проигрывателя Windows Media с Microsoft Office**</span><span class="sxs-lookup"><span data-stu-id="e7a9e-132">**Using the Windows Media Player Control with Microsoft Office**</span></span>](using-the-windows-media-player-control-with-microsoft-office.md)
</dt> </dl>

 

 




