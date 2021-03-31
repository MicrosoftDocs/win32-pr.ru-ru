---
title: Протокол ВМПДВД
description: Протокол ВМПДВД
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Проигрыватель Windows Media, протоколы
- Объектная модель проигрывателя Windows Media, протоколы
- Объектная модель, протоколы
- Элемент управления ActiveX проигрывателя Windows Media, протоколы для объектной модели
- Элемент управления ActiveX, протоколы для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, протоколы для объектной модели
- Проигрыватель Windows Media Mobile, протоколы для объектной модели
- протоколы, объектная модель проигрывателя Windows Media
- протоколы, ВМПДВД
- Протокол ВМПДВД
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329664"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="dd266-113">Протокол ВМПДВД</span><span class="sxs-lookup"><span data-stu-id="dd266-113">WMPDVD Protocol</span></span>

<span data-ttu-id="dd266-114">Протокол ВМПДВД позволяет указать носитель с помощью синтаксиса URL-адреса DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="dd266-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="dd266-115">Это общая форма протокола:</span><span class="sxs-lookup"><span data-stu-id="dd266-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="dd266-116">Сегмент *диска* — буква DVD-дисковода; Он не включает двоеточие, обычно используемое с описателями дисков.</span><span class="sxs-lookup"><span data-stu-id="dd266-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="dd266-117">Этот сегмент всегда является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dd266-117">This segment is always required.</span></span>

<span data-ttu-id="dd266-118">Сегмент *заголовка* — это номер названия для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dd266-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="dd266-119">Это не является обязательным, если вы не хотите запускать воспроизведение в определенном заголовке или в определенной главе определенного заголовка.</span><span class="sxs-lookup"><span data-stu-id="dd266-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="dd266-120">Сегмент *главы* — это номер главы для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dd266-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="dd266-121">Это необязательно, если вы не хотите начинать воспроизведение в определенной главе определенного заголовка.</span><span class="sxs-lookup"><span data-stu-id="dd266-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="dd266-122">Аргумент ContentDir — это путь к видео \_ TS. Файл ИФО, который может находиться в локальном хранилище или в общей сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="dd266-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="dd266-123">Если включить этот сегмент, сегмент *диска* будет пропущен, хотя он по-прежнему необходим.</span><span class="sxs-lookup"><span data-stu-id="dd266-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="dd266-124">Если также включить сегмент *заголовка* или *заголовок* и сегменты *глав* , они будут относиться к содержимому DVD-диска, указанному в сегменте ContentDir, а не к сегменту *диска* .</span><span class="sxs-lookup"><span data-stu-id="dd266-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="dd266-125">В следующем примере используется протокол ВМПДВД для воспроизведения DVD-диска с самого начала, как если бы он был запущен автоматически.</span><span class="sxs-lookup"><span data-stu-id="dd266-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="dd266-126">В следующем примере используется протокол ВМПДВД для воспроизведения DVD-диска с начала указанного заголовка.</span><span class="sxs-lookup"><span data-stu-id="dd266-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="dd266-127">В следующем примере используется протокол ВМПДВД для воспроизведения DVD-диска из указанной главы.</span><span class="sxs-lookup"><span data-stu-id="dd266-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="dd266-128">В следующем примере используется протокол ВМПДВД для воспроизведения содержимого DVD-диска из локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="dd266-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="dd266-129">Строка *пути* заканчивается папкой, содержащей видео \_ служб терминалов. Файл ИФО; Он не включает имя файла.</span><span class="sxs-lookup"><span data-stu-id="dd266-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="dd266-130">В этом примере значение сегмента *диска* не оказывает никакого влияния, хотя оно является обязательным, а воспроизведение начинается в главе 4 заголовка 2.</span><span class="sxs-lookup"><span data-stu-id="dd266-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="dd266-131">Чтобы назначить строку ВМПДВД для свойства **URL-адреса** , требуется проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="dd266-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd266-132">См. также</span><span class="sxs-lookup"><span data-stu-id="dd266-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd266-133">**Поддерживаемые протоколы и типы файлов**</span><span class="sxs-lookup"><span data-stu-id="dd266-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




