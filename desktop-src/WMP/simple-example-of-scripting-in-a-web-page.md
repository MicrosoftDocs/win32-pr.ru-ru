---
title: Простой пример создания сценариев на веб-странице
description: Простой пример создания сценариев на веб-странице
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
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
- Элемент управления ActiveX проигрывателя Windows Media, пример сценария
- Элемент управления ActiveX проигрывателя Windows Media для мобильных устройств, пример сценария
- Элемент управления ActiveX, пример сценария
- внедрение, веб-страницы
- Внедрение веб-страниц, пример сценария
- Пример сценария для внедрения веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105700731"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="718a4-119">Простой пример создания сценариев на веб-странице</span><span class="sxs-lookup"><span data-stu-id="718a4-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="718a4-120">Вы можете легко внедрить элемент управления проигрывателя Windows Media в HTML-файл, используя любой язык сценариев, распознаваемый браузером.</span><span class="sxs-lookup"><span data-stu-id="718a4-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="718a4-121">В следующем простом примере используется Microsoft JScript для создания страницы, которая будет воспроизводить файл при нажатии кнопки, и прекращает воспроизведение файла при нажатии на другую кнопку.</span><span class="sxs-lookup"><span data-stu-id="718a4-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="718a4-122">Элемент управления ActiveX проигрывателя Windows Media можно внедрить на веб-страницу, выполнив следующие четыре шага:</span><span class="sxs-lookup"><span data-stu-id="718a4-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="718a4-123">Создайте веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="718a4-123">Create the webpage.</span></span>
2.  <span data-ttu-id="718a4-124">Добавьте тег объекта.</span><span class="sxs-lookup"><span data-stu-id="718a4-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="718a4-125">Добавьте пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="718a4-125">Add a user interface.</span></span> <span data-ttu-id="718a4-126">В этом случае две кнопки.</span><span class="sxs-lookup"><span data-stu-id="718a4-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="718a4-127">Добавьте несколько строк кода, чтобы ответить, когда пользователь щелкнет одну из созданных кнопок.</span><span class="sxs-lookup"><span data-stu-id="718a4-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="718a4-128">Создание веб-страницы</span><span class="sxs-lookup"><span data-stu-id="718a4-128">Creating the Web Page</span></span>

<span data-ttu-id="718a4-129">Первым шагом является создание допустимой веб-страницы HTML.</span><span class="sxs-lookup"><span data-stu-id="718a4-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="718a4-130">Следующий код является минимальным необходимым для создания пустой, но допустимой HTML-страницы:</span><span class="sxs-lookup"><span data-stu-id="718a4-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="718a4-131">Добавление тега объекта</span><span class="sxs-lookup"><span data-stu-id="718a4-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="718a4-132">После создания веб-страницы необходимо добавить тег объекта.</span><span class="sxs-lookup"><span data-stu-id="718a4-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="718a4-133">Он определяет элемент управления ActiveX для браузера и настраивает начальные определения.</span><span class="sxs-lookup"><span data-stu-id="718a4-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="718a4-134">Тег объекта необходимо поместить в тело кода.</span><span class="sxs-lookup"><span data-stu-id="718a4-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="718a4-135">Если поместить его в текст, будет отображаться пользовательский интерфейс по умолчанию проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="718a4-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="718a4-136">Если вы хотите создать собственный пользовательский интерфейс, установите атрибуты Height и Width равными 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="718a4-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="718a4-137">Можно также задать *проигрыватель*. **uiMode** свойство в «невидимый», если необходимо скрыть элемент управления, но на странице зарезервируется место для него.</span><span class="sxs-lookup"><span data-stu-id="718a4-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="718a4-138">При предоставлении настраиваемого пользовательского интерфейса рекомендуется использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="718a4-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="718a4-139">Требуются следующие атрибуты тега объекта:</span><span class="sxs-lookup"><span data-stu-id="718a4-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="718a4-140">ID</span><span class="sxs-lookup"><span data-stu-id="718a4-140">ID</span></span>

<span data-ttu-id="718a4-141">Имя, которое будет использоваться другими частями кода для обнаружения и использования элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="718a4-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="718a4-142">Можно выбрать любое имя, если оно еще не используется HTML, HTML-расширениями или используемым языком сценариев.</span><span class="sxs-lookup"><span data-stu-id="718a4-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="718a4-143">В этом примере используется имя Player, но можно также вызвать его «MyPlayer» или что-то другое.</span><span class="sxs-lookup"><span data-stu-id="718a4-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="718a4-144">Просто выберите уникальное для этой веб-страницы имя.</span><span class="sxs-lookup"><span data-stu-id="718a4-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="718a4-145">КЛАССА</span><span class="sxs-lookup"><span data-stu-id="718a4-145">CLASSID</span></span>

<span data-ttu-id="718a4-146">Очень большое шестнадцатеричное число, уникальное для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="718a4-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="718a4-147">Только один элемент управления имеет это число и является элементом управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="718a4-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="718a4-148">Чтобы предотвратить типографские ошибки, можно скопировать и вставить этот номер из документации.</span><span class="sxs-lookup"><span data-stu-id="718a4-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="718a4-149">Версии элемента управления проигрывателя Windows Media до версии 7,0 имеют другой идентификатор CLASSID.</span><span class="sxs-lookup"><span data-stu-id="718a4-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="718a4-150">Добавление пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="718a4-150">Adding a User Interface</span></span>

<span data-ttu-id="718a4-151">HTML обеспечивает обширное множество элементов пользовательского интерфейса, позволяя пользователю взаимодействовать с веб-страницей, щелкая, нажимая клавиши и другие действия пользователя.</span><span class="sxs-lookup"><span data-stu-id="718a4-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="718a4-152">Добавление нескольких кнопок ввода — самый простой способ предоставить быстрый пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="718a4-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="718a4-153">Следующий код создает две кнопки, которые могут отвечать пользователю.</span><span class="sxs-lookup"><span data-stu-id="718a4-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="718a4-154">При нажатии одной кнопки запускается поток мультимедиа, а другая кнопка останавливается.</span><span class="sxs-lookup"><span data-stu-id="718a4-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="718a4-155">Имя кнопки используется для распознавания кнопки в коде. значение — это метка, которая будет отображаться на кнопке, а атрибут onclick определяет, какая часть кода скрипта будет вызываться при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="718a4-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="718a4-156">Добавление кода скрипта</span><span class="sxs-lookup"><span data-stu-id="718a4-156">Adding Scripting Code</span></span>

<span data-ttu-id="718a4-157">Код скрипта добавляет интерактивность на страницу.</span><span class="sxs-lookup"><span data-stu-id="718a4-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="718a4-158">Код скрипта может реагировать на события, вызывать методы и изменять свойства времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="718a4-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="718a4-159">Расширенные скрипты заключаются в набор тегов СКРИПТа.</span><span class="sxs-lookup"><span data-stu-id="718a4-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="718a4-160">Тег SCRIPT сообщает браузеру, где находится код скрипта, и определяет язык сценариев.</span><span class="sxs-lookup"><span data-stu-id="718a4-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="718a4-161">Если язык не определен, языком по умолчанию будет Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="718a4-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="718a4-162">Рекомендуется заключать сценарий в теги комментариев HTML, чтобы браузеры, не поддерживающие скрипты, не отображали код в виде текста.</span><span class="sxs-lookup"><span data-stu-id="718a4-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="718a4-163">Поместите тег СКРИПТа в любом месте текста HTML-файла и внедрите код, заключенный в комментарий, в открывающий и закрывающий теги СКРИПТа.</span><span class="sxs-lookup"><span data-stu-id="718a4-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="718a4-164">Следующий пример кода Microsoft JScript вызывает элемент управления проигрывателя Windows Media и выполняет соответствующее действие в ответ на нажатие соответствующей кнопки.</span><span class="sxs-lookup"><span data-stu-id="718a4-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="718a4-165">Пример функции Стартмеуп вызывается при нажатии кнопки Play, а функция Шутмедовн вызывается при нажатии кнопки "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="718a4-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="718a4-166">Код внутри Стартмеуп использует свойство URL-адреса для определения пути к носителю.</span><span class="sxs-lookup"><span data-stu-id="718a4-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="718a4-167">Воспроизведение носителя начнется немедленно.</span><span class="sxs-lookup"><span data-stu-id="718a4-167">The media will start playing immediately.</span></span>

<span data-ttu-id="718a4-168">Код Шутмедовн вызывает метод **останавливает** объекта **Controls** .</span><span class="sxs-lookup"><span data-stu-id="718a4-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="718a4-169">Обратите внимание, что объект **Controls** вызывается через свойство **Controls** объекта **Player** , имеющего значение идентификатора "Player".</span><span class="sxs-lookup"><span data-stu-id="718a4-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="718a4-170">Ниже приведен полный пример кода.</span><span class="sxs-lookup"><span data-stu-id="718a4-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="718a4-171">Обратите внимание, что необходимо указать допустимый URL-адрес в качестве допустимого имени файла в свойстве URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="718a4-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="718a4-172">В этом случае предполагается, что файл Лауре. WMA находится в том же каталоге, что и HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="718a4-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="718a4-173">См. также</span><span class="sxs-lookup"><span data-stu-id="718a4-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="718a4-174">**Использование элемента управления проигрывателя Windows Media на веб-странице**</span><span class="sxs-lookup"><span data-stu-id="718a4-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




