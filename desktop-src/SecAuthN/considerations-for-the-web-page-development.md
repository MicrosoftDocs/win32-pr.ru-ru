---
description: Посредник веб-аутентификации основан на тех же технологиях, что и Power Internet Explorer в Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Рекомендации по разработке веб-страниц
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346005"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="bb0bc-103">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="bb0bc-103">Considerations for the web page development</span></span>

<span data-ttu-id="bb0bc-104">Посредник веб-аутентификации основан на тех же технологиях, что и Power Internet Explorer в Windows.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="bb0bc-105">Однако из-за специального назначения этого компонента некоторые функции Internet Explorer были отключены или заблокированы для конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="bb0bc-106">Кроме того, посредник веб-проверки подлинности предоставляет выделенный канал ведения журнала событий для устранения проблем с страницами, которые он обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="bb0bc-107">Режим документов Internet Explorer 10 Standard</span><span class="sxs-lookup"><span data-stu-id="bb0bc-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="bb0bc-108">Брокер веб-проверки подлинности отображает все страницы в стандартном режиме IE10.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="bb0bc-109">Вы можете использовать средства разработчика в Internet Explorer, чтобы увидеть, как страница работает в различных режимах документов.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="bb0bc-110">Дополнительные сведения о совместимости Internet Explorer 10 см. в статьях MSDN для [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb0bc-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="bb0bc-111">Отключенные и заблокированные компоненты</span><span class="sxs-lookup"><span data-stu-id="bb0bc-111">Disabled and locked down features</span></span>

<span data-ttu-id="bb0bc-112">Некоторые функции Internet Explorer полностью отключены или заблокированы для определенных значений, которые нельзя изменить в свойствах Интернета операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="bb0bc-113">Компонент</span><span class="sxs-lookup"><span data-stu-id="bb0bc-113">Feature</span></span>                            | <span data-ttu-id="bb0bc-114">Status</span><span class="sxs-lookup"><span data-stu-id="bb0bc-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0bc-115">API кэша приложений ("Аппкаче")</span><span class="sxs-lookup"><span data-stu-id="bb0bc-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="bb0bc-116">Выключено</span><span class="sxs-lookup"><span data-stu-id="bb0bc-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="bb0bc-117">Журнал ссылок</span><span class="sxs-lookup"><span data-stu-id="bb0bc-117">Link history</span></span>                       | <span data-ttu-id="bb0bc-118">Выключено</span><span class="sxs-lookup"><span data-stu-id="bb0bc-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="bb0bc-119">Временные файлы</span><span class="sxs-lookup"><span data-stu-id="bb0bc-119">Temporary files</span></span>                    | <span data-ttu-id="bb0bc-120">Активировано</span><span class="sxs-lookup"><span data-stu-id="bb0bc-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="bb0bc-121">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="bb0bc-121">Cookies</span></span>                            | <span data-ttu-id="bb0bc-122">Файлы cookie сеансов включены.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-122">Session cookies are enabled.</span></span> <span data-ttu-id="bb0bc-123">Сохраненные файлы cookie разрешены, но могут автоматически очищаться, если только посредник веб-аутентификации не находится в режиме единого входа.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="bb0bc-124">Дополнительные сведения см. в разделе единый вход.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="bb0bc-125">База данных индекса</span><span class="sxs-lookup"><span data-stu-id="bb0bc-125">Index DB</span></span>                           | <span data-ttu-id="bb0bc-126">Выключено</span><span class="sxs-lookup"><span data-stu-id="bb0bc-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="bb0bc-127">Хранилище DOM</span><span class="sxs-lookup"><span data-stu-id="bb0bc-127">DOM storage</span></span>                        | <span data-ttu-id="bb0bc-128">Выключено</span><span class="sxs-lookup"><span data-stu-id="bb0bc-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="bb0bc-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="bb0bc-129">ActiveX</span></span>                            | <span data-ttu-id="bb0bc-130">Выключено</span><span class="sxs-lookup"><span data-stu-id="bb0bc-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="bb0bc-131">Загружаемые файлы</span><span class="sxs-lookup"><span data-stu-id="bb0bc-131">File downloads</span></span>                     | <span data-ttu-id="bb0bc-132">Выключено</span><span class="sxs-lookup"><span data-stu-id="bb0bc-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="bb0bc-133">Требование HTTPS</span><span class="sxs-lookup"><span data-stu-id="bb0bc-133">HTTPS requirement</span></span>

<span data-ttu-id="bb0bc-134">Первый URL-адрес, который будет использоваться приложением для взаимодействия с поставщиком в Интернете, должен быть HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="bb0bc-135">Измерение для различных размеров окна</span><span class="sxs-lookup"><span data-stu-id="bb0bc-135">Dimension for different window sizes</span></span>

<span data-ttu-id="bb0bc-136">Приложение Windows 8 может отображаться на различных размерах, таких как полноэкранный режим, окно с измененным размером или на чудо-странице, например "поделиться чудо".</span><span class="sxs-lookup"><span data-stu-id="bb0bc-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="bb0bc-137">В зависимости от того, какой макет окна отображается посредником веб-проверки подлинности, размер, с которым должны работать веб-страницы, может отличаться.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="bb0bc-138">Дополнительные сведения см. в разделе [рекомендации по изменению размера в узкие макеты](/previous-versions/windows/hh465371(v=win.10)) и [рекомендации по предоставлению общего доступа к содержимому](/previous-versions/windows/hh465251(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="bb0bc-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="bb0bc-139">Веб-страница должна использовать запросы мультимедиа CSS для проверки размера, с которым он должен работать, и соответствующим образом разметить его.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="bb0bc-140">Однако эта страница не должна быть разработана на основе заданных здесь пикселов, и ее можно масштабировать до различных размеров.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="bb0bc-141">Размеры, указанные в этом документе, могут быть изменены в будущих версиях ОС.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="bb0bc-142">Если страница не может вместить всю информацию в выделенном пространстве (например, длинный список разрешений, запрашиваемых приложением), посредник веб-проверки подлинности предоставит полосы прокрутки, позволяющие пользователю прокручивать страницу по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="bb0bc-143">Кроме того, можно увеличить масштаб сжатия для сенсорных устройств и Ctrl + Колесико мыши для настольных и переносных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="bb0bc-144">Для тестирования различных факторов масштабирования используется [пример приложения SDK посредника веб-проверки подлинности](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) , загруженный в Microsoft Visual Studio Professional 2012, что позволяет имитировать полноэкранный режим и изменить размер состояний.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="bb0bc-145">В дополнение к различным макетам, описанным выше, обязательно протестируйте страницу на разных ориентациях экрана (например, книжную или альбомную), а также на разных языковых стандартах и языках, включая специальные возможности, такие как параметр «сделать все больше» включен.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="bb0bc-146">Доступны следующие макеты:</span><span class="sxs-lookup"><span data-stu-id="bb0bc-146">The available layouts are:</span></span>

-   [<span data-ttu-id="bb0bc-147">Во весь экран</span><span class="sxs-lookup"><span data-stu-id="bb0bc-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="bb0bc-148">Окно с измененным размером</span><span class="sxs-lookup"><span data-stu-id="bb0bc-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="bb0bc-149">Представление чудо</span><span class="sxs-lookup"><span data-stu-id="bb0bc-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="bb0bc-150">Представление средства выбора файлов</span><span class="sxs-lookup"><span data-stu-id="bb0bc-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="bb0bc-151">Во весь экран</span><span class="sxs-lookup"><span data-stu-id="bb0bc-151">Full screen</span></span>

<span data-ttu-id="bb0bc-152">Для полноэкранного макета используются следующие измерения веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="bb0bc-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="bb0bc-153">Ширина: 566 пикселей</span><span class="sxs-lookup"><span data-stu-id="bb0bc-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="bb0bc-154">Высота: высота экрана (зависит от разрешения экрана)</span><span class="sxs-lookup"><span data-stu-id="bb0bc-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="bb0bc-155">В следующем примере показан пользовательский интерфейс посредника веб-проверки подлинности в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![Пример пользовательского интерфейса посредника веб-проверки подлинности в полноэкранном режиме](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="bb0bc-157">Изменен</span><span class="sxs-lookup"><span data-stu-id="bb0bc-157">Resized</span></span>

<span data-ttu-id="bb0bc-158">Для окна с измененным размером размеры веб-страницы могут быть:</span><span class="sxs-lookup"><span data-stu-id="bb0bc-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="bb0bc-159">Ширина: 260 пикселей</span><span class="sxs-lookup"><span data-stu-id="bb0bc-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="bb0bc-160">Высота: высота экрана (зависит от разрешения экрана)</span><span class="sxs-lookup"><span data-stu-id="bb0bc-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="bb0bc-161">В следующем примере показан пользовательский интерфейс посредника веб-проверки подлинности в окне с измененным размером на веб-странице XBox.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="bb0bc-162">Обратите внимание, что пользовательский интерфейс посредника веб-проверки подлинности находится только в правой части снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![Пример пользовательского интерфейса посредника веб-проверки подлинности в окне с измененным размером](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="bb0bc-164">Представление чудо</span><span class="sxs-lookup"><span data-stu-id="bb0bc-164">Charm view</span></span>

<span data-ttu-id="bb0bc-165">Для представления чудо используются следующие измерения веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="bb0bc-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="bb0bc-166">Ширина: 566 пикселей</span><span class="sxs-lookup"><span data-stu-id="bb0bc-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="bb0bc-167">Высота: высота экрана (зависит от разрешения экрана)</span><span class="sxs-lookup"><span data-stu-id="bb0bc-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="bb0bc-168">В следующем примере показан пользовательский интерфейс посредника веб-проверки подлинности в представлении чудо.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![в примере показан пользовательский интерфейс посредника веб-проверки подлинности в представлении чудо](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="bb0bc-170">Представление средства выбора файлов</span><span class="sxs-lookup"><span data-stu-id="bb0bc-170">File picker view</span></span>

<span data-ttu-id="bb0bc-171">Для представления средства выбора файлов используются следующие измерения веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="bb0bc-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="bb0bc-172">Ширина: 566 пикселей</span><span class="sxs-lookup"><span data-stu-id="bb0bc-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="bb0bc-173">Высота: высота экрана (зависит от разрешения экрана)</span><span class="sxs-lookup"><span data-stu-id="bb0bc-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="bb0bc-174">В следующем примере показан пользовательский интерфейс посредника веб-проверки подлинности в представлении средства выбора файлов.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![в примере показан пользовательский интерфейс посредника веб-проверки подлинности в представлении средства выбора файлов.](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="bb0bc-176">Нет новых окон по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bb0bc-176">No new windows by default</span></span>

<span data-ttu-id="bb0bc-177">По умолчанию ни один из URL-адресов не приведет к открытию нового окна, а будет отображаться в окне брокера веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="bb0bc-178">Сюда входит метод Window. Open JavaScript, "Target" атрибута гиперссылок или когда пользователь использует механизм Ctrl + щелчок для принудительного открытия нового окна.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="bb0bc-179">Исключением из этого правила является то, что веб-страница объявляет ссылку как защищенную для перехода в браузере, как описано в разделе Настройка целевого объекта гиперссылок.</span><span class="sxs-lookup"><span data-stu-id="bb0bc-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb0bc-180">См. также</span><span class="sxs-lookup"><span data-stu-id="bb0bc-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb0bc-181">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="bb0bc-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="bb0bc-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="bb0bc-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
