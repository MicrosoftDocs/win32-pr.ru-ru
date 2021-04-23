---
title: Отладка кода
description: Отладка кода
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Обложки проигрывателя Windows Media, отладка кода
- обложки, отладка кода
- Отладка кода для обложек
- Обложки проигрывателя Windows Media, ведение журнала
- обложки, ведение журнала
- функции ведения журнала в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332032"
---
# <a name="debugging-code"></a><span data-ttu-id="46e4c-109">Отладка кода</span><span class="sxs-lookup"><span data-stu-id="46e4c-109">Debugging Code</span></span>

<span data-ttu-id="46e4c-110">Часто возникает необходимость увидеть, что происходит внутри обложки.</span><span class="sxs-lookup"><span data-stu-id="46e4c-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="46e4c-111">Это можно сделать с помощью текстового элемента управления или файла журнала.</span><span class="sxs-lookup"><span data-stu-id="46e4c-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="46e4c-112">Вы можете временно создать **текстовый** элемент и поместить его в часть обложки.</span><span class="sxs-lookup"><span data-stu-id="46e4c-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="46e4c-113">Например, можно использовать следующий код для создания **текстового** элемента:</span><span class="sxs-lookup"><span data-stu-id="46e4c-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="46e4c-114">Например, если вы хотите увидеть текущее расположение цифрового содержимого в проигрывателе Windows Media, можно использовать код, аналогичный приведенному ниже, чтобы отобразить текущую координату в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="46e4c-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="46e4c-115">Запись отладочной информации в файл журнала</span><span class="sxs-lookup"><span data-stu-id="46e4c-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="46e4c-116">Чтобы включить или отключить отладку, измените значение следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="46e4c-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="46e4c-117">**HKEY \_ текущее \_ пользовательское \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ предпочтения \\ скриптдебуггинг**</span><span class="sxs-lookup"><span data-stu-id="46e4c-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="46e4c-118">Если задать значение 1, ведение журнала будет включено.</span><span class="sxs-lookup"><span data-stu-id="46e4c-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="46e4c-119">Если задать значение 0 (по умолчанию), ведение журнала отключено.</span><span class="sxs-lookup"><span data-stu-id="46e4c-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="46e4c-120">Если ведение журнала включено, файл будет помещен на компьютер пользователя в той же папке, что и обложка.</span><span class="sxs-lookup"><span data-stu-id="46e4c-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="46e4c-121">Файл будет называться "*filename* \_ 0 \_log.txt", где *filename* — это имя файла обложки.</span><span class="sxs-lookup"><span data-stu-id="46e4c-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="46e4c-122">Код в обложке может записывать текст в этот файл с помощью *темы*. метод **логстринг** .</span><span class="sxs-lookup"><span data-stu-id="46e4c-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="46e4c-123">Это может быть полезно, если нужно определить, что происходит внутри кода во время его работы.</span><span class="sxs-lookup"><span data-stu-id="46e4c-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="46e4c-124">Обратите внимание, что текстовый файл кодируется символами Юникода.</span><span class="sxs-lookup"><span data-stu-id="46e4c-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="46e4c-125">Если ведение журнала включено и вы установили систему разработки, которая предоставляет возможности отладки (например, Microsoft Visual Studio), исключения, которые не обрабатываются кодом скрипта, приведут к открытию диалогового окна предупреждения отладчика для каждого исключения.</span><span class="sxs-lookup"><span data-stu-id="46e4c-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="46e4c-126">Это полезная функция, помогающая в отладке кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="46e4c-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="46e4c-127">Кроме того, можно вручную подключить процесс проигрывателя Windows Media к отладчику при включенном ведении журнала.</span><span class="sxs-lookup"><span data-stu-id="46e4c-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="46e4c-128">Этот пакет SDK включает образец обложки «Logging», который демонстрирует функциональные возможности ведения журнала в обложках.</span><span class="sxs-lookup"><span data-stu-id="46e4c-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="46e4c-129">Дополнительные сведения об использовании примеров см. в разделе [образцы](samples.md).</span><span class="sxs-lookup"><span data-stu-id="46e4c-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46e4c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="46e4c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46e4c-131">**О обложках**</span><span class="sxs-lookup"><span data-stu-id="46e4c-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




