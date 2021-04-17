---
title: Использование Хтмлвиев с Интернет-магазинами
description: Использование Хтмлвиев с Интернет-магазинами
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Интернет-магазины проигрывателя Windows Media, Хтмлвиев
- Интернет-магазины, Хтмлвиев
- Тип 1 Интернет-магазины, Хтмлвиев
- Тип 2 Интернет-магазинов, Хтмлвиев
- Хтмлвиев, Интернет-магазины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691372"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="9da29-108">Использование Хтмлвиев с Интернет-магазинами</span><span class="sxs-lookup"><span data-stu-id="9da29-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="9da29-109">Проигрыватель Windows Media запрашивает у пользователей разрешение на отображение содержимого Хтмлвиев в текущий **момент**.</span><span class="sxs-lookup"><span data-stu-id="9da29-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="9da29-110">Интернет-магазины могут отключить этот запрос, указав базовое значение URL-адреса в элементе **хтмлвиев** документа serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="9da29-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="9da29-111">Когда проигрыватель Windows Media открывает список воспроизведения, указывающий отображаемое содержимое Хтмлвиев, проигрыватель сравнивает базовый URL-адрес из документа ServiceInfo текущего активного оперативного хранилища с базовым URL-адресом содержимого Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="9da29-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="9da29-112">Если они совпадают, проигрыватель Windows Media отображает содержимое Хтмлвиев без запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="9da29-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9da29-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9da29-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da29-114">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9da29-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="9da29-115">**Хтмлвиев, элемент**</span><span class="sxs-lookup"><span data-stu-id="9da29-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="9da29-116">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="9da29-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




