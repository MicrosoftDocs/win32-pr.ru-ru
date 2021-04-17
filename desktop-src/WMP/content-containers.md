---
title: Контейнеры содержимого
description: Контейнеры содержимого
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Интернет-магазины проигрывателя Windows Media, контейнеры содержимого
- Интернет-магазины, контейнеры содержимого
- Тип 1 Интернет-магазины, контейнеры содержимого
- Интернет-магазины проигрывателя Windows Media, интерфейс Ивмпконтентконтаинер
- Интернет-магазины, интерфейс Ивмпконтентконтаинер
- Тип 1 Интернет-магазины, интерфейс Ивмпконтентконтаинер
- Проигрыватель Windows Media, контейнеры содержимого
- Проигрыватель Windows Media, интерфейс Ивмпконтентконтаинер
- контейнеры содержимого
- ивмпконтентконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105691476"
---
# <a name="content-containers"></a><span data-ttu-id="4ba14-113">Контейнеры содержимого</span><span class="sxs-lookup"><span data-stu-id="4ba14-113">Content Containers</span></span>

<span data-ttu-id="4ba14-114">Проигрыватель Windows Media использует контейнеры содержимого для представления цифрового мультимедийного содержимого в рамках подписки на скачивание или покупку.</span><span class="sxs-lookup"><span data-stu-id="4ba14-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="4ba14-115">Контейнер содержимого представлен интерфейсом **ивмпконтентконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="4ba14-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="4ba14-116">Контейнер содержимого может содержать список связанных содержимого, таких как альбом, или набор несвязанных элементов содержимого или *дорожек*.</span><span class="sxs-lookup"><span data-stu-id="4ba14-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="4ba14-117">Вы можете использовать интерфейс **ивмпконтентконтаинер** для перечисления дорожек контейнера содержимого и получения стоимости каждой дорожки. Также можно получить сведения о контейнере содержимого, например идентификатор контейнера, тип содержимого в контейнере и общую стоимость для дорожек в контейнере (которая может отличаться от суммы цен отдельных курсов, как в случае покупки в альбоме).</span><span class="sxs-lookup"><span data-stu-id="4ba14-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="4ba14-118">Чтобы предоставить механизм для упаковки нескольких контейнеров содержимого в один объект, проигрыватель Windows Media поддерживает интерфейс **ивмпконтентконтаинерлист** .</span><span class="sxs-lookup"><span data-stu-id="4ba14-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="4ba14-119">**Ивмпконтентконтаинерлист** предоставляет методы для перечисления и извлечения контейнеров содержимого в списке.</span><span class="sxs-lookup"><span data-stu-id="4ba14-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="4ba14-120">Чтобы узнать, представляет ли список контейнера содержимого покупку или загрузку подписки, вызовите [ивмпконтентконтаинерлист:: жеттрансактионтипе](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) , чтобы получить значение [вмптрансактионтипе](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .</span><span class="sxs-lookup"><span data-stu-id="4ba14-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ba14-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4ba14-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ba14-122">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="4ba14-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4ba14-123">**Интерфейс Ивмпконтентконтаинер**</span><span class="sxs-lookup"><span data-stu-id="4ba14-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="4ba14-124">**Интерфейс Ивмпконтентконтаинерлист**</span><span class="sxs-lookup"><span data-stu-id="4ba14-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




