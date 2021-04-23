---
description: В этом разделе описываются рекомендации по проектированию веб-страниц, использующих брокер веб-проверки подлинности для входа в систему.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Советы и рекомендации по разработке веб-страниц для аутентификации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344365"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="6e2e5-103">Советы и рекомендации по разработке веб-страниц для аутентификации</span><span class="sxs-lookup"><span data-stu-id="6e2e5-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="6e2e5-104">В этом разделе описываются рекомендации по проектированию веб-страниц, использующих брокер веб-проверки подлинности для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="6e2e5-105">Использование метатегов</span><span class="sxs-lookup"><span data-stu-id="6e2e5-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="6e2e5-106">Использование стилей CSS в Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e2e5-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="6e2e5-107">Использование цвета и тем</span><span class="sxs-lookup"><span data-stu-id="6e2e5-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="6e2e5-108">Выравнивание</span><span class="sxs-lookup"><span data-stu-id="6e2e5-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="6e2e5-109">Проектирование для привязки</span><span class="sxs-lookup"><span data-stu-id="6e2e5-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="6e2e5-110">Разработка для быстрого и гибкого входа в систему</span><span class="sxs-lookup"><span data-stu-id="6e2e5-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="6e2e5-111">Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="6e2e5-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="6e2e5-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6e2e5-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="6e2e5-113">Использование метатегов</span><span class="sxs-lookup"><span data-stu-id="6e2e5-113">Use of metatags</span></span>

<span data-ttu-id="6e2e5-114">С помощью метатегов поставщик "Contoso Social" может указать заголовок, значок и цвет заголовка.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="6e2e5-115">В примере HTML-файла (WebAuthLogin.html) это делается с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="6e2e5-116">Это позволяет Windows интегрировать присутствие поставщика в заголовке пользовательского интерфейса, выделенном красным прямоугольником на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![страница входа с заголовком Contoso в пользовательском интерфейсе](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="6e2e5-118">Использование стилей CSS в Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e2e5-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="6e2e5-119">Указанная таблица стилей УИ-Лигхт. CSS — это таблица стилей Windows 8, используемая приложениями Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="6e2e5-120">Он определяет стиль приложений Магазина Windows для типографских и стандартных элементов управления, таких как кнопки, текстовые поля, гиперссылки и флажки, чтобы они были сенсорно понятны.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="6e2e5-121">При проектировании и адаптации страниц веб-авторизации для Windows 8 мы рекомендуем использовать эту таблицу стилей как есть и обновлять ее по мере необходимости, если веб-страница по-прежнему соответствует рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="6e2e5-122">Например, если у вас есть специальная таблица стилей, которая будет выглядеть так, как на веб-странице, то лучше убедиться в том, что предоставляемая им стилизация удобна так же, как стандартные гиперссылки Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="6e2e5-123">Это важно для базы потребителя, использующей Windows 8 на сенсорных устройствах.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="6e2e5-124">Использование цвета и тем</span><span class="sxs-lookup"><span data-stu-id="6e2e5-124">Use of color and themes</span></span>

<span data-ttu-id="6e2e5-125">В этом образце демонстрируется продуманное использование цвета несколькими различными способами.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="6e2e5-126">Белый фон для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-126">White background for the web page.</span></span> <span data-ttu-id="6e2e5-127">Как можно узнать из предыдущего снимка экрана, веб-страница размещается на белой поверхности, которая охватывает ширину экрана.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="6e2e5-128">Чтобы убедиться, что веб-страница интегрируется с поверхностью, рекомендуется, чтобы на веб-странице был белый фон.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="6e2e5-129">Окраска элементов управления на основе цвета торговой марки.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="6e2e5-130">CSS-файл семе-Колорс. CSS предоставляет стили для переопределения стандартных цветов элементов управления в таблице стилей пользовательского интерфейса, чтобы они совпадали с элементами управления с цветом заголовка.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="6e2e5-131">Например, на следующем снимке экрана кнопки и гиперссылки принимают цвета, производные от цвета заголовка.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![снимок экрана кнопок и текста, имеющих тот же цвет, что и заголовок](images/wab-figure11.png)
-   <span data-ttu-id="6e2e5-133">Цвет заголовка.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-133">Header color.</span></span> <span data-ttu-id="6e2e5-134">Использование цвета торговой марки Contoso в заголовке создает единую индивидуальность для торговой марки поставщика в пользовательском интерфейсе системы.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="6e2e5-135">Выравнивание</span><span class="sxs-lookup"><span data-stu-id="6e2e5-135">Alignment</span></span>

<span data-ttu-id="6e2e5-136">Сама веб-страница не имеет отступов слева или справа, чтобы разрешить типографское выравнивание с заголовком в верхнем колонтитуле слева и значком в верхнем колонтитуле справа.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="6e2e5-137">Также обратите внимание, что кнопки всегда расположены по правому нижнему краю на веб-странице (и отображаются справа по значку в заголовке).</span><span class="sxs-lookup"><span data-stu-id="6e2e5-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="6e2e5-138">Это лучшая практика, так как пользователи Windows 8 будут привычны для последовательностей диалоговых окон с кнопками в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="6e2e5-139">Проектирование для привязки</span><span class="sxs-lookup"><span data-stu-id="6e2e5-139">Designing for snap</span></span>

<span data-ttu-id="6e2e5-140">На следующем рисунке вы видите страницы входа и разрешения в состоянии привязки.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="6e2e5-141">представление "привязка" экрана входа</span><span class="sxs-lookup"><span data-stu-id="6e2e5-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="6e2e5-142">.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-142">.</span></span> ![<span data-ttu-id="6e2e5-143">представление "привязка" страницы "разрешения"</span><span class="sxs-lookup"><span data-stu-id="6e2e5-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="6e2e5-144">В примере файла УИ-вебаус. CSS можно увидеть использование запросов к мультимедиа, которые оптимизируют макет страницы для состояния привязки на основе ширины, доступной для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="6e2e5-145">Фрагмент кода, заключенный в следующую область, реализует CSS, предназначенный для состояния привязки.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="6e2e5-146">В Windows 8 ширина состояния привязки составляет 320 пикселей.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="6e2e5-147">Страница веб-аутентификации занимает 260 пикселей в пользовательском интерфейсе выше.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="6e2e5-148">Мы используем значение максимальной ширины с достаточной маржой, поэтому код запроса мультимедиа поставщика не привязан к точной ширине состояния привязки.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="6e2e5-149">При адаптации приложения к представлению прикрепления важно, чтобы пользователь не потерял никакой контекст, который есть в других представлениях возможностей веб-проверки подлинности (Full, Fill или чудо), но он очень полезен для повторной структуризации макета и иерархии элементов на странице, чтобы информация, необходимая для сохранения контекста, была видимой и интерактивной.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="6e2e5-150">Мы назвали некоторые примеры того, как пример хвоста веб-страницы для состояния привязки.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="6e2e5-151">Например, для страницы входа в состоянии привязки свойство Width текстового поля ввода (как указано в УИ-Лигхт. CSS) было переопределено и было задано как меньшее числовое значение, чтобы текстовое поле не было горизонтально обрезано.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="6e2e5-152">Другой пример: в состоянии привязки размер шрифта заголовков h1 и H2 уменьшается до 20 PT и 11 пт с 42 пт и 20 пт соответственно.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="6e2e5-153">Это делается в соответствии с пандусом типа Windows 8 и оптимизирует текст для более компактного в измененном окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="6e2e5-154">В качестве другого примера обратите внимание, что размеры значков на странице разрешения меньше (Сравните со страницей полного представления выше).</span><span class="sxs-lookup"><span data-stu-id="6e2e5-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="6e2e5-155">Опять же, это делается для того, чтобы хранить контекст, в то же время заменяя ресурсы разработки для них более оптимальными для измененного окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="6e2e5-156">Разработка для быстрого и гибкого входа в систему</span><span class="sxs-lookup"><span data-stu-id="6e2e5-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="6e2e5-157">На ранних этапах разработки этой веб-страницы мы сделали заявляйте, что одна из них лучше всего подходит для быстрого и гибкого входа в систему.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="6e2e5-158">Таким же пользовательским интерфейсом, который является наиболее наглядным в последовательности, является поле username и Password (имя пользователя и пароль) на странице входа для быстрого ввода учетных данных.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="6e2e5-159">Хотя мы определили, что существуют и другие распространенные сценарии, такие как получение пароля и создание ссылок на заявления о конфиденциальности, лучшее место в Интернете — это лучший вариант.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="6e2e5-160">Для всех потоков, не связанных с безопасной веб-аутентификацией, рекомендуется перейти в браузер.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="6e2e5-161">Это показано в примере файла HTML (WebAuthLogin.html) следующим образом: `<meta name="mswebdialog-newwindowurl" content="*" />` открывает все веб-страницы, связанные с, из страницы имя входа или разрешения в браузере пользователя по умолчанию, где пользователь может выполнить эти последовательности, а затем вернуться к приложению для входа.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="6e2e5-162">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="6e2e5-162">Security Considerations</span></span>

<span data-ttu-id="6e2e5-163">В следующих статьях приводятся рекомендации по написанию безопасного кода C++.</span><span class="sxs-lookup"><span data-stu-id="6e2e5-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="6e2e5-164">Рекомендации по обеспечению безопасности для C++</span><span class="sxs-lookup"><span data-stu-id="6e2e5-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="6e2e5-165">[Шаблоны & рекомендации по обеспечению безопасности для приложений](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="6e2e5-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e2e5-166">См. также</span><span class="sxs-lookup"><span data-stu-id="6e2e5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e2e5-167">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="6e2e5-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="6e2e5-168">Вопросы и ответы по брокеру веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="6e2e5-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="6e2e5-169">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="6e2e5-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="6e2e5-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="6e2e5-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
