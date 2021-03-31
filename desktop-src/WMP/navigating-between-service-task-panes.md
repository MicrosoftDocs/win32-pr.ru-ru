---
title: Переход между областями задач службы
description: Переход между областями задач службы
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Интернет-магазины проигрывателя Windows Media, Навигация
- Интернет-магазины, Навигация
- Тип 2 Интернет-магазинов, Навигация
- Интернет-магазины проигрывателя Windows Media, области задач службы
- Интернет-магазины, области задач службы
- Введите 2 Интернет-магазина, области задач службы
- Интернет-магазины проигрывателя Windows Media, области задач
- Интернет-магазины, области задач
- Введите 2 Интернет-магазина, области задач
- Навигация по типу 2 Интернет-магазинов
- Проигрыватель Windows Media, области задач службы
- Проигрыватель Windows Media, области задач
- области задач службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329979"
---
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="13b20-116">Переход между областями задач службы</span><span class="sxs-lookup"><span data-stu-id="13b20-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="13b20-117">Для перехода между областями задач службы в проигрывателе Windows Media используется метод **навигатетаскпанеурл** , доступный с помощью объекта **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="13b20-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="13b20-118">При использовании этого метода необходимо указать значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="13b20-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="13b20-119">*бстркэйнаме*.</span><span class="sxs-lookup"><span data-stu-id="13b20-119">*bstrKeyName*.</span></span> <span data-ttu-id="13b20-120">Это имя ключа Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="13b20-120">This is the key name of the online store.</span></span> <span data-ttu-id="13b20-121">При переходе в Интернет-магазине используйте имя ключа текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="13b20-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="13b20-122">*бстртаскпане*.</span><span class="sxs-lookup"><span data-stu-id="13b20-122">*bstrTaskPane*.</span></span> <span data-ttu-id="13b20-123">Эта строка содержит имя области задач службы, к которой необходимо выполнить переход.</span><span class="sxs-lookup"><span data-stu-id="13b20-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="13b20-124">*бстрпарамс*.</span><span class="sxs-lookup"><span data-stu-id="13b20-124">*bstrParams*.</span></span> <span data-ttu-id="13b20-125">Эта строка содержит параметры строки запроса, которые необходимо добавить к URL-адресу веб-страницы, размещенной в области задач службы, к которой необходимо выполнить переход.</span><span class="sxs-lookup"><span data-stu-id="13b20-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="13b20-126">Управление навигацией осуществляется с помощью создаваемой веб-страницы, которая называется «Навигация».</span><span class="sxs-lookup"><span data-stu-id="13b20-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="13b20-127">URL-адрес страницы навигации задается элементом **navigate** в документе serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="13b20-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="13b20-128">При вызове **Навигатетаскпанеурл** проигрыватель Windows Media открывает страницу Навигация, а не веб-страницу, заданную элементами **ServiceTask1**, **ServiceTask2** или **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="13b20-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="13b20-129">Это страница навигации, которая получает строку запроса, указанную параметром *бстрпарамс*.</span><span class="sxs-lookup"><span data-stu-id="13b20-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="13b20-130">Страница Навигация должна содержать правила, определяющие, какое содержимое отображается в области задач службы после перемещения.</span><span class="sxs-lookup"><span data-stu-id="13b20-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="13b20-131">Например, предположим, что вы хотите, чтобы пользователи щелкнули ссылку для перехода с **ServiceTask1** на **ServiceTask2**.</span><span class="sxs-lookup"><span data-stu-id="13b20-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="13b20-132">Для создания ссылки можно использовать следующий HTML-код:</span><span class="sxs-lookup"><span data-stu-id="13b20-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="13b20-133">Когда пользователь щелкает ссылку на видео, проигрыватель Windows Media переключается на **ServiceTask2** и открывает страницу навигации, добавляя следующую строку запроса к URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="13b20-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="13b20-134">Параметр From определяет страницу, с которой пользователь щелкнул ссылку, а параметр to определяет номер области задач службы, которой он хочет перейти.</span><span class="sxs-lookup"><span data-stu-id="13b20-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="13b20-135">(Обратите внимание, что нет ничего особенного об этих параметрах.</span><span class="sxs-lookup"><span data-stu-id="13b20-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="13b20-136">Вы можете использовать любые параметры для любой выбранной цели.)</span><span class="sxs-lookup"><span data-stu-id="13b20-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="13b20-137">Например, в следующем примере кода показан элемент **navigate** в документе serviceInfo:</span><span class="sxs-lookup"><span data-stu-id="13b20-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="13b20-138">Итоговый URL-адрес, полный запрос со строкой запроса, показан в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="13b20-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="13b20-139">В следующем примере кода показана страница «Навигация»:</span><span class="sxs-lookup"><span data-stu-id="13b20-139">The following example code shows the navigate page:</span></span>


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



<span data-ttu-id="13b20-140">Приведенный выше код просто создает URL-адрес и перенаправляет в него браузер.</span><span class="sxs-lookup"><span data-stu-id="13b20-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="13b20-141">Сначала код получает значения из строки запроса URL-адреса и самой строки запроса.</span><span class="sxs-lookup"><span data-stu-id="13b20-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="13b20-142">Для определения отображаемой страницы используется значение параметра to.</span><span class="sxs-lookup"><span data-stu-id="13b20-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="13b20-143">Затем в URL-адрес добавляется исходная строка запроса.</span><span class="sxs-lookup"><span data-stu-id="13b20-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="13b20-144">И, наконец, он перейдет в браузер, используя URL-адрес следующего вида:</span><span class="sxs-lookup"><span data-stu-id="13b20-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="13b20-145">При таком способе навигации не забудьте указать [External. селектедтаскпане](external-selectedtaskpane.md) , чтобы правильно выделить кнопку задачи.</span><span class="sxs-lookup"><span data-stu-id="13b20-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="13b20-146">**Предупреждение об ошибке** Будьте внимательны при использовании параметров строки запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="13b20-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="13b20-147">Веб-страницы Хтмлвиев могут предоставляться любым пользователем, который создает список воспроизведения ASX.</span><span class="sxs-lookup"><span data-stu-id="13b20-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="13b20-148">Это означает, что вредоносные веб-сайты могут передавать значения строк запросов в Интернет-магазин с помощью **навигатетаскпанеурл**.</span><span class="sxs-lookup"><span data-stu-id="13b20-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="13b20-149">Необходимо спланировать эту возможность, чтобы обеспечить безопасность Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="13b20-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="13b20-150">Например, если в Интернет-магазине просто отображается значение строки запроса для пользователя, вредоносный веб-сайт может отобразить непредвиденный текст.</span><span class="sxs-lookup"><span data-stu-id="13b20-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13b20-151">См. также</span><span class="sxs-lookup"><span data-stu-id="13b20-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13b20-152">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="13b20-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="13b20-153">**Элемент Navigate**</span><span class="sxs-lookup"><span data-stu-id="13b20-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="13b20-154">**Навигация для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="13b20-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




