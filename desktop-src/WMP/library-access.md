---
title: Доступ к библиотеке
description: Доступ к библиотеке
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Проигрыватель Windows Media, Библиотека
- Объектная модель проигрывателя Windows Media, Библиотека
- Объектная модель, Библиотека
- Проигрыватель Windows Media Mobile, Библиотека для объектной модели
- Элемент управления ActiveX проигрывателя Windows Media, Библиотека для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, Библиотека для объектной модели
- Элемент управления ActiveX, Библиотека для объектной модели
- Библиотека проигрывателя Windows Media, доступ
- Библиотека, доступ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329875"
---
# <a name="library-access"></a><span data-ttu-id="0cfe2-112">Доступ к библиотеке</span><span class="sxs-lookup"><span data-stu-id="0cfe2-112">Library Access</span></span>

<span data-ttu-id="0cfe2-113">Свойствам и методам объектной модели проигрывателя Windows Media, обращающимся к библиотеке, требуется доступ только для чтения или для чтения и записи в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="0cfe2-114">Библиотека содержит сведения, которые некоторые пользователи хотят хранить частным и которые должны быть доступны или изменены только с согласия пользователя.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="0cfe2-115">Для Windows Media Player 9 Series или более поздней версии можно программно определить уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="0cfe2-116">Чтобы определить текущий уровень доступа, предоставленный коду, извлеките *Параметры*. Свойство **медиаакцессригхтс** .</span><span class="sxs-lookup"><span data-stu-id="0cfe2-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="0cfe2-117">Это свойство возвращает "None", "Read" или "Full" (чтение и запись).</span><span class="sxs-lookup"><span data-stu-id="0cfe2-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="0cfe2-118">Чтобы запросить определенные права доступа, вызовите *Параметры*. метод **рекуестмедиаакцессригхтс** , передающий параметр, указывающий запрашиваемый уровень.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="0cfe2-119">Метод отображает сообщение пользователю, объясняющему запрошенный уровень доступа, и возвращает **логическое** значение, указывающее, предоставлен ли доступ.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="0cfe2-120">Определенные права доступа предоставляются автоматически в зависимости от того, где выполняется код относительно компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="0cfe2-121">Если веб-страница или программа находится на компьютере пользователя, по умолчанию предоставляются права полного доступа.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="0cfe2-122">Веб-страницы имеют доступ для чтения к *проигрывателю*. **куррентмедиа**, *Player*. **куррентплайлист** и *мультимедиа*. **саурцеурл** , когда веб-страница находится в зоне безопасности Internet Explorer, которая является той же или меньше ограниченной, чем зона безопасности элемента мультимедиа или списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="0cfe2-123">В диапазоне от минимального ограничения до наибольшего ограничения зоны безопасности — это **Доверенная** зона (включая локальный компьютер пользователя), зона **местной интрасети** , зона **Интернета** и **ограниченная** зона.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="0cfe2-124">Например, веб-страница в зоне **локальной интрасети** имеет права полного доступа к *проигрывателю*. **куррентмедиа** , когда соответствующий элемент мультимедиа находится в локальной интрасети или Интернете, но права доступа должны быть запрошены для элементов мультимедиа, расположенных на локальном компьютере пользователя или на веб-сайте в **доверенной** зоне.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="0cfe2-125">Следует протестировать веб-приложения или приложение на базе Windows во всех зонах безопасности, которые он может столкнуться.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="0cfe2-126">Приложение должно быть спроектировано таким образом, чтобы правильно обрабатывать отказ запросов доступа.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="0cfe2-127">Версии объектной модели проигрывателя Windows Media до Windows Media 9 серии не включают **медиаакцессригхтс** или **рекуестмедиаакцессригхтс**.</span><span class="sxs-lookup"><span data-stu-id="0cfe2-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="0cfe2-128">Эти более ранние версии проигрывателя Windows Media позволяют пользователю задавать уровни доступа с помощью диалогового окна **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="0cfe2-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cfe2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0cfe2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cfe2-130">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="0cfe2-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="0cfe2-131">**Работа с библиотекой**</span><span class="sxs-lookup"><span data-stu-id="0cfe2-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




