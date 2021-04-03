---
title: Ссылки на обложки в URL-адресах
description: Ссылки на обложки в URL-адресах
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Обложки проигрывателя Windows Media, URL-ссылки
- обложки, URL-ссылки
- URL-ссылки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779583"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="72b1f-106">Ссылки на обложки в URL-адресах</span><span class="sxs-lookup"><span data-stu-id="72b1f-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="72b1f-107">Если для загрузки файла мультимедиа, который будет воспроизводиться проигрывателем Windows Media, используется URL-адрес, можно запросить использование определенной обложки с этим файлом.</span><span class="sxs-lookup"><span data-stu-id="72b1f-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="72b1f-108">Если обложка уже установлена на компьютере пользователя, она будет использоваться. в противном случае будет использоваться Предыдущая обложка.</span><span class="sxs-lookup"><span data-stu-id="72b1f-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="72b1f-109">Чтобы запросить обложку, добавьте в конец URL-адреса следующее:</span><span class="sxs-lookup"><span data-stu-id="72b1f-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="72b1f-110">*скиннаме* — имя обложки, которую необходимо запросить.</span><span class="sxs-lookup"><span data-stu-id="72b1f-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="72b1f-111">Не используйте кавычки вокруг имени обложки.</span><span class="sxs-lookup"><span data-stu-id="72b1f-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="72b1f-112">Например, чтобы запросить использование обложки хеадспаце, введите следующий URL-адрес http:</span><span class="sxs-lookup"><span data-stu-id="72b1f-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="72b1f-113">См. также</span><span class="sxs-lookup"><span data-stu-id="72b1f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72b1f-114">**О обложках**</span><span class="sxs-lookup"><span data-stu-id="72b1f-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




