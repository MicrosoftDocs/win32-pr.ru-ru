---
title: Разработка Client-Side
description: Скрипты на серверных страницах HTML взаимодействуют с мастером заказа отпечатков в сети, в котором он размещен. Это взаимодействие осуществляется через методы и свойства, к которым обращается объект Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- мастера публикации, Разработка на стороне клиента
- Window. external, мастера публикации
- мастера публикации, Window. external
- мастера публикации, рекомендации по проектированию
- мастера публикации, мастер заказа принтера в сети
- Мастер заказа отпечатков в сети, проект на стороне клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987486"
---
# <a name="client-side-design"></a><span data-ttu-id="ad112-110">Разработка Client-Side</span><span class="sxs-lookup"><span data-stu-id="ad112-110">Client-Side Design</span></span>

<span data-ttu-id="ad112-111">Скрипты на серверных страницах HTML взаимодействуют с мастером заказа отпечатков в сети, в котором он размещен.</span><span class="sxs-lookup"><span data-stu-id="ad112-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="ad112-112">Это взаимодействие осуществляется через методы и свойства, к которым обращается объект **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="ad112-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="ad112-113">В этом документе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="ad112-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="ad112-114">Методы и свойства</span><span class="sxs-lookup"><span data-stu-id="ad112-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="ad112-115">Вопросы проектирования</span><span class="sxs-lookup"><span data-stu-id="ad112-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="ad112-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ad112-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="ad112-117">Методы и свойства</span><span class="sxs-lookup"><span data-stu-id="ad112-117">Methods and Properties</span></span>

<span data-ttu-id="ad112-118">Следующие методы и свойства доступны через объект **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="ad112-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="ad112-119">**финалбакк**</span><span class="sxs-lookup"><span data-stu-id="ad112-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="ad112-120">**финалнекст**</span><span class="sxs-lookup"><span data-stu-id="ad112-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="ad112-121">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="ad112-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="ad112-122">**пасспортаусентикате**</span><span class="sxs-lookup"><span data-stu-id="ad112-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="ad112-123">**сесеадертекст**</span><span class="sxs-lookup"><span data-stu-id="ad112-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="ad112-124">**сетвизардбуттонс**</span><span class="sxs-lookup"><span data-stu-id="ad112-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="ad112-125">[**Заголовок**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad112-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="ad112-126">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="ad112-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="ad112-127">Скрипт страницы на стороне сервера вызывает эти методы для уведомления клиента о событиях во время процедуры публикации.</span><span class="sxs-lookup"><span data-stu-id="ad112-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="ad112-128">Давайте рассмотрим [**финалбакк**](/windows/desktop/shell/iwebwizardhost-finalback) в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="ad112-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="ad112-129">Когда в мастере отображается первая страница HTML на стороне сервера, она делает то же самое с знанием дескрипторов для страниц мастера ранее и после размещенных HTML-страниц.</span><span class="sxs-lookup"><span data-stu-id="ad112-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="ad112-130">На этом этапе в нашем примере пользователь, расположенный на первой HTML-странице, нажимает кнопку « **назад** ».</span><span class="sxs-lookup"><span data-stu-id="ad112-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="ad112-131">Мастер отправляет уведомление об этом событии на сервер.</span><span class="sxs-lookup"><span data-stu-id="ad112-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="ad112-132">При получении этого сообщения сценарий на стороне сервера ссылается на обработчик **onback** для этого события, который, как это первая HTML-страница, вызывает метод **финалбакк** .</span><span class="sxs-lookup"><span data-stu-id="ad112-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="ad112-133">Это приводит к тому, что мастер переходит на страницу мастера, отображаемую перед вводом пользовательского интерфейса на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="ad112-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="ad112-134">Полное описание этих методов и свойств см. в документации по объектам [**вебвизардхост**](/windows/desktop/shell/webwizardhost) и [**неввдевентс**](/windows/desktop/shell/newwdevents) .</span><span class="sxs-lookup"><span data-stu-id="ad112-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="ad112-135">Вопросы проектирования</span><span class="sxs-lookup"><span data-stu-id="ad112-135">Design Considerations</span></span>

<span data-ttu-id="ad112-136">HTML-код, выполняющий каждую страницу на стороне сервера, обычно отображается на панели мастера.</span><span class="sxs-lookup"><span data-stu-id="ad112-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="ad112-137">При проектировании этих страниц следует помнить, что размер окна мастера изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="ad112-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="ad112-138">Таким образом, страницы должны быть сконструированы и изменяться размерами, чтобы полосы прокрутки можно было избегать, когда это возможно, чтобы предоставить пользователю гладкую навигацию через мастер.</span><span class="sxs-lookup"><span data-stu-id="ad112-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="ad112-139">Каждая HTML-страница должна также предоставлять обработчик для событий **onback**, **onback** и **onback** .</span><span class="sxs-lookup"><span data-stu-id="ad112-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="ad112-140">Обработчик **OnNext** также будет работать с событием **завершения** .</span><span class="sxs-lookup"><span data-stu-id="ad112-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="ad112-141">Страница, не реализующая функцию **Onback** , считается недопустимой и приведет к отображению страницы ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad112-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad112-142">См. также</span><span class="sxs-lookup"><span data-stu-id="ad112-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad112-143">**вебвизардхост**</span><span class="sxs-lookup"><span data-stu-id="ad112-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="ad112-144">**неввдевентс**</span><span class="sxs-lookup"><span data-stu-id="ad112-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="ad112-145">Проектирование на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="ad112-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 