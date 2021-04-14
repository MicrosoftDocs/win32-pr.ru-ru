---
title: Использование URL-адреса и смены сервера
description: Использование URL-адреса и смены сервера
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Списки воспроизведения метафайлов Windows Media, смены URL-адресов
- списки воспроизведения, переключение URL-адресов
- списки воспроизведения метафайлов, смены URL-адресов
- Списки воспроизведения метафайлов Windows Media, переключение серверов
- списки воспроизведения, переключение серверов
- списки воспроизведения метафайлов, переключение серверов
- Списки воспроизведения метафайлов Windows Media, переключение протоколов
- списки воспроизведения, переключение протоколов
- списки воспроизведения метафайлов, переключение протоколов
- Проигрыватель Windows Media, смены URL-адресов
- Проигрыватель Windows Media, переключение сервера
- Проигрыватель Windows Media, переключение протоколов
- Смены URL-адресов
- переключения сервера
- Переключение протоколов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330256"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="cda9f-118">Использование URL-адреса и смены сервера</span><span class="sxs-lookup"><span data-stu-id="cda9f-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="cda9f-119">Списки воспроизведения метафайлов можно использовать для предоставления средств автоматического перехода к альтернативным источникам содержимого, когда поток недоступен или не может быть воспроизведен.</span><span class="sxs-lookup"><span data-stu-id="cda9f-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="cda9f-120">Этот метод продолжения можно использовать для указания источников одного и того же содержимого на разных серверах или на разных типах серверов.</span><span class="sxs-lookup"><span data-stu-id="cda9f-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="cda9f-121">Например, можно указать первую альтернативу на другом сервере Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cda9f-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="cda9f-122">Если это содержимое не удается воспроизвести, клиент может перейти на второй вариант на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="cda9f-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="cda9f-123">Проигрыватель Windows Media автоматически пытается выполнить переход на разные протоколы в соответствии с настройками свойств Windows Media, прежде чем пытаться URL-адреса смены в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cda9f-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="cda9f-124">Установите переключение сервера и протокола, поместив несколько элементов **ref** в последовательность в одном элементе **entry** .</span><span class="sxs-lookup"><span data-stu-id="cda9f-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="cda9f-125">Каждый **ссылочный** элемент указывает альтернативное расположение или протокол для файла мультимедиа или потока.</span><span class="sxs-lookup"><span data-stu-id="cda9f-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="cda9f-126">Пример кода</span><span class="sxs-lookup"><span data-stu-id="cda9f-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="cda9f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cda9f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cda9f-128">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="cda9f-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="cda9f-129">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="cda9f-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




