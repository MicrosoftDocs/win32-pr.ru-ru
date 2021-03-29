---
title: Обеспечение открытия проигрывателем Windows Media содержимого Хтмлвиев
description: Обеспечение открытия проигрывателем Windows Media содержимого Хтмлвиев
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Списки воспроизведения метафайлов Windows Media, проигрыватель Windows Media открытие содержимого Хтмлвиев
- списки воспроизведения, проигрыватель Windows Media открытие содержимого Хтмлвиев
- списки воспроизведения метафайлов, проигрыватель Windows Media открытие содержимого Хтмлвиев
- Списки воспроизведения метафайлов Windows Media, открытие содержимого Хтмлвиев
- списки воспроизведения, открытие содержимого Хтмлвиев
- списки воспроизведения метафайлов, открытие содержимого Хтмлвиев
- открытие содержимого Хтмлвиев
- Проигрыватель Windows Media, открытие содержимого Хтмлвиев
- Проигрыватель Windows Media, Хтмлвиев содержимое
- Хтмлвиев, открытие содержимого
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776511"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="a00a7-113">Обеспечение открытия проигрывателем Windows Media содержимого Хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="a00a7-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="a00a7-114">В настоящее время проигрыватель Windows Media 9 Series и проигрыватель Windows Media 10 являются единственными игроками, которые поддерживают параметр *хтмлвиев* в файлах ASX.</span><span class="sxs-lookup"><span data-stu-id="a00a7-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="a00a7-115">Это означает, что необходимо предпринять шаги по обеспечению воспроизведения содержимого Хтмлвиев в этих версиях проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a00a7-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="a00a7-116">Сначала необходимо определить, установлен ли на компьютере пользователя ряд проигрывателя Windows Media 9 или Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="a00a7-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="a00a7-117">В состав пакета SDK для проигрывателя Windows Media входит полный пример, демонстрирующий обнаружение различных версий проигрывателя Windows Media в различных веб-браузерах.</span><span class="sxs-lookup"><span data-stu-id="a00a7-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="a00a7-118">Несмотря на то, что полный анализ образца обнаружения выходит за рамки этого раздела, существует ряд основных шагов, которые можно предпринять, чтобы определить, какая версия проигрывателя Windows Media используется на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="a00a7-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="a00a7-119">В простейшей форме обнаружение проигрывателя Windows Media включает внедрение элемента управления проигрывателя в веб-страницу, ссылающуюся на содержимое Хтмлвиев, а затем проверку значения, полученного *проигрывателем*. Свойство **versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="a00a7-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="a00a7-120">Убедившись, что у пользователя установлен ряд Windows Media Player 9 или Windows Media Player 10, можно открыть содержимое в проигрывателе в полноэкранном режиме с помощью метода [Player. опенплайер](player-openplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="a00a7-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="a00a7-121">Метод **опенплайер** гарантирует, что содержимое будет отображаться в **воспроизводимой** функции проигрывателя в полноэкранном режиме, а не в обложке, в режиме мини-проигрывателя или в другом проигрывателе, который зарегистрировал себя как программа по умолчанию для файлов с расширением. ASX, но не поддерживает хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="a00a7-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="a00a7-122">Однако после отображения содержимого пользователь получает полный контроль над проигрывателем Windows Media, что означает, что он может выбрать отображение функции, отличной от **воспроизводимого**, переключения в режим обложки или даже выход из проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="a00a7-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="a00a7-123">В следующем примере кода создается веб-страница для Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a00a7-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="a00a7-124">На этой странице открывается ASX-файл, указывающий веб-страницу Хтмлвиев, которая отображается в полноэкранном режиме при установленном проигрывателе Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a00a7-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="a00a7-125">Код в предыдущем примере внедряет элемент управления проигрывателя Windows Media со свойством **uiMode** , установленным в "Невидимый", а атрибуты Height и Width проигрывателя устанавливаются в ноль.</span><span class="sxs-lookup"><span data-stu-id="a00a7-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="a00a7-126">Это связано с тем, что веб-страница не требует первоначального отображения пользовательского интерфейса управления проигрывателем — ему нужен только доступ к объектной модели проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="a00a7-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="a00a7-127">На странице также отображается кнопка ввода, позволяющая пользователю воспроизвести ASX-файл.</span><span class="sxs-lookup"><span data-stu-id="a00a7-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="a00a7-128">Когда пользователь нажимает кнопку Воспроизвести ASX, выполняется функция Microsoft JScript Плайаскс.</span><span class="sxs-lookup"><span data-stu-id="a00a7-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="a00a7-129">Эта функция сначала извлекает значение для свойства Player **versionInfo** , используя метод JScript **parseInt** для проверки числового значения извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a00a7-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="a00a7-130">Если числовое значение больше или равно 9 (то есть у пользователя установлен ряд Windows Media 9 Series), код скрипта вызывает метод **опенплайер** , передавая URL-адрес файла. ASX, содержащего параметр хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="a00a7-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="a00a7-131">Этот метод открывает ASX-файл с помощью проигрывателя Windows Media в полноэкранном режиме, воспроизводит мультимедийное содержимое в файле списка ASX и отображает веб-содержимое Хтмлвиев в **воспроизводимой** функции.</span><span class="sxs-lookup"><span data-stu-id="a00a7-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="a00a7-132">Если числовое значение строки версии не больше или равно 9 (это означает, что на компьютере пользователя не установлен проигрыватель Windows Media 9 или более поздней версии), код скрипта изменяет **uiMode** элемента управления проигрывателя на «Full», устанавливает новую ширину и высоту для элемента управления, а затем открывает ASX-файл во внедренном проигрывателе, указывая значение свойства **URL** .</span><span class="sxs-lookup"><span data-stu-id="a00a7-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="a00a7-133">В этом случае мультимедийное содержимое воспроизводится на веб-странице, но все значения Хтмлвиев, указанные в файле ASX, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="a00a7-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="a00a7-134">Способ воспроизведения содержимого, когда у пользователя не установлен проигрыватель Windows Media 9 Series или проигрыватель Windows Media 10 не работает.</span><span class="sxs-lookup"><span data-stu-id="a00a7-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="a00a7-135">В предыдущем примере показано, как указать, что содержимое воспроизводится на веб-странице, а не в полноэкранном проигрывателе, игнорируя содержимое Хтмлвиев в процессе.</span><span class="sxs-lookup"><span data-stu-id="a00a7-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="a00a7-136">Есть и другие подходы, которые вы можете предпринять.</span><span class="sxs-lookup"><span data-stu-id="a00a7-136">There are other approaches you might take.</span></span> <span data-ttu-id="a00a7-137">Например, можно предложить пользователю установить более новую версию проигрывателя Windows Media, сделав эту версию проигрывателя требованием к воспроизведению цифрового мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="a00a7-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a00a7-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a00a7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a00a7-139">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a00a7-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="a00a7-140">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="a00a7-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="a00a7-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="a00a7-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




