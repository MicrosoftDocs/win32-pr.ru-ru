---
title: Типы отображаемых текста
description: Типы отображаемых текста
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Обложки Windows Media Player для мобильных устройств, текст
- текст в обложках, типы вывода
- обложки, текст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775101"
---
# <a name="text-display-types"></a><span data-ttu-id="d0ea1-106">Типы отображаемых текста</span><span class="sxs-lookup"><span data-stu-id="d0ea1-106">Text Display Types</span></span>

<span data-ttu-id="d0ea1-107">В обложку не нужно включать текст, но при этом может потребоваться много экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-107">You do not need to include text displays in your skin, but there are many instances where you might want to.</span></span> <span data-ttu-id="d0ea1-108">Например, может потребоваться включить линейок поиска, чтобы разрешить пользователю переходить к любой позиции в элементе мультимедиа, но можно также включить отображение текста, в котором отображается количество секунд, прошедших с момента запуска текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-108">For example, you might want to include a Seek trackbar to allow the user to move to any position in the media item, but you also might want to include a text display that shows the number of seconds that have elapsed since the current media item started playing.</span></span>

<span data-ttu-id="d0ea1-109">**Отображаемые поля**</span><span class="sxs-lookup"><span data-stu-id="d0ea1-109">**Display Boxes**</span></span>

<span data-ttu-id="d0ea1-110">Ниже приведены несколько атрибутов, которые может отображать текстовый элемент.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-110">The following are several attributes a text element can display:</span></span>

-   <span data-ttu-id="d0ea1-111">Время</span><span class="sxs-lookup"><span data-stu-id="d0ea1-111">Time</span></span>
-   <span data-ttu-id="d0ea1-112">Списком</span><span class="sxs-lookup"><span data-stu-id="d0ea1-112">Playlist</span></span>
-   <span data-ttu-id="d0ea1-113">Track\#</span><span class="sxs-lookup"><span data-stu-id="d0ea1-113">Track\#</span></span>
-   <span data-ttu-id="d0ea1-114">\#Трассировк</span><span class="sxs-lookup"><span data-stu-id="d0ea1-114">\#Tracks</span></span>
-   <span data-ttu-id="d0ea1-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d0ea1-115">Title</span></span>
-   <span data-ttu-id="d0ea1-116">Автор</span><span class="sxs-lookup"><span data-stu-id="d0ea1-116">Author</span></span>
-   <span data-ttu-id="d0ea1-117">Авторские права</span><span class="sxs-lookup"><span data-stu-id="d0ea1-117">Copyright</span></span>
-   <span data-ttu-id="d0ea1-118">Имя файла</span><span class="sxs-lookup"><span data-stu-id="d0ea1-118">Filename</span></span>
-   <span data-ttu-id="d0ea1-119">филенамикст</span><span class="sxs-lookup"><span data-stu-id="d0ea1-119">FilenameExt</span></span>
-   <span data-ttu-id="d0ea1-120">Bitrate</span><span class="sxs-lookup"><span data-stu-id="d0ea1-120">Bitrate</span></span>
-   <span data-ttu-id="d0ea1-121">Частота</span><span class="sxs-lookup"><span data-stu-id="d0ea1-121">Frequency</span></span>
-   <span data-ttu-id="d0ea1-122">Состояние</span><span class="sxs-lookup"><span data-stu-id="d0ea1-122">Status</span></span>
-   <span data-ttu-id="d0ea1-123">волперцент</span><span class="sxs-lookup"><span data-stu-id="d0ea1-123">VolPercent</span></span>

<span data-ttu-id="d0ea1-124">Дополнительные сведения о типах вывода текста см. в разделе " [текст](text.md) " ссылки на обложку.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-124">For more information about text display types, see the [Text](text.md) section of the Skin Reference.</span></span>

<span data-ttu-id="d0ea1-125">**Бегущая строка**</span><span class="sxs-lookup"><span data-stu-id="d0ea1-125">**Scrolling Marquee**</span></span>

<span data-ttu-id="d0ea1-126">Помимо использования отдельных текстовых элементов, можно объединить один или несколько атрибутов в бегущую строку текста.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-126">In addition to using the individual text elements, you can combine one or more attributes into a scrolling text marquee.</span></span> <span data-ttu-id="d0ea1-127">Это полезно, если требуется отобразить группирование связанных текстовых данных в небольшой области.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-127">This is useful if you want to display a grouping of related text information in a small area.</span></span> <span data-ttu-id="d0ea1-128">Например, можно отобразить заголовок, автора и сведения об авторских правах в области.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-128">For example, you could display Title, Author, and Copyright information in a Marquee.</span></span>

<span data-ttu-id="d0ea1-129">Дополнительные сведения о создании области текста см. в разделе " [область](marquee.md) " в справочнике по обложкам.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-129">For more information about creating a text marquee, see the [Marquee](marquee.md) section of the Skin Reference.</span></span>

<span data-ttu-id="d0ea1-130">**Отображение состояния**</span><span class="sxs-lookup"><span data-stu-id="d0ea1-130">**Status Display**</span></span>

<span data-ttu-id="d0ea1-131">Другим типом отображаемого текста является отображение состояния.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-131">Another type of text display is the status display.</span></span> <span data-ttu-id="d0ea1-132">Это позволяет автоматически отображать сведения о текущем состоянии проигрывателя Windows Media Mobile.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-132">This lets you automatically display information about the current state of Windows Media Player Mobile.</span></span> <span data-ttu-id="d0ea1-133">Например, при отображении состояния отображается уведомление пользователя при буферизации элемента мультимедиа, чтобы было очевидно, что проигрыватель работает.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-133">For example, the status display will inform the user when a media item is buffering so that it is evident that the Player is working.</span></span>

<span data-ttu-id="d0ea1-134">В отображаемом состоянии отображаются следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="d0ea1-134">The following messages appear in the status display:</span></span>

-   <span data-ttu-id="d0ea1-135">ответов</span><span class="sxs-lookup"><span data-stu-id="d0ea1-135">Buffering</span></span>
-   <span data-ttu-id="d0ea1-136">Соединение</span><span class="sxs-lookup"><span data-stu-id="d0ea1-136">Connecting</span></span>
-   <span data-ttu-id="d0ea1-137">Пауза</span><span class="sxs-lookup"><span data-stu-id="d0ea1-137">Paused</span></span>
-   <span data-ttu-id="d0ea1-138">Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="d0ea1-138">Playing</span></span>
-   <span data-ttu-id="d0ea1-139">Ready</span><span class="sxs-lookup"><span data-stu-id="d0ea1-139">Ready</span></span>
-   <span data-ttu-id="d0ea1-140">Остановлена</span><span class="sxs-lookup"><span data-stu-id="d0ea1-140">Stopped</span></span>

> [!Note]  
> <span data-ttu-id="d0ea1-141">При воспроизведении элемента мультимедиа отображение состояния будет проходить через подзаголовок, исполнителя, альбом, жанр и текущую скорость.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-141">When a media item is playing, the status display will rotate through subtitle, artist, album, genre, and current bitrate.</span></span>

 

<span data-ttu-id="d0ea1-142">Сведения о создании представления состояния с помощью элемента Status см. в разделе [состояние](status.md) ссылки на обложку. Тем не менее предпочтительнее использовать атрибут Status в элементе text, а не в элементе Status.</span><span class="sxs-lookup"><span data-stu-id="d0ea1-142">For information about creating a status display through the Status element, see the [Status](status.md) section of the Skin Reference; however, it is preferred that you use the status attribute in the Text element instead of the Status element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0ea1-143">См. также</span><span class="sxs-lookup"><span data-stu-id="d0ea1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0ea1-144">**Мобильные функции проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d0ea1-144">**Windows Media Player Mobile Functionality**</span></span>](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




