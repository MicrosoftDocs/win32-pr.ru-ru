---
title: Документ ServiceInfo для Интернет-магазина типа 2
description: Документ ServiceInfo для Интернет-магазина типа 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Интернет-магазины проигрывателя Windows Media, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 2 Интернет-магазинов, документ ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068119"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="05857-107">Документ ServiceInfo для Интернет-магазина типа 2</span><span class="sxs-lookup"><span data-stu-id="05857-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="05857-108">Поставщики интернет-магазинов типа 2 должны предоставлять Майкрософт URL-адрес XML-документа, описывающего Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="05857-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="05857-109">Проигрыватель Windows Media 10 и проигрыватель Windows Media 11 используйте этот документ, чтобы определить, как настроить пользовательский интерфейс для размещения интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="05857-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="05857-110">В проигрывателе Windows Media 10 документ ServiceInfo содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="05857-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="05857-111">Сведения о настройке областей задач, отображаемых проигрывателем Windows Media при активном Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="05857-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="05857-112">Интернет-магазин может иметь одну, две или три области задач.</span><span class="sxs-lookup"><span data-stu-id="05857-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="05857-113">Сведения, используемые для настройки кнопок области задач, например текст кнопки, цвет кнопки и подсказки для кнопок.</span><span class="sxs-lookup"><span data-stu-id="05857-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="05857-114">URL-адреса изображений, которые проигрыватель Windows Media отображает для обнаружения интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="05857-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="05857-115">URL-адреса веб-страниц, предоставляемые Интернет-магазином для размещения проигрывателя Windows Media в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="05857-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="05857-116">Сведения о том, как программа установки проигрывателя Windows Media должна настроить первое сетевое хранилище, которое видит пользователь.</span><span class="sxs-lookup"><span data-stu-id="05857-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="05857-117">В проигрывателе Windows Media 11 документ ServiceInfo содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="05857-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="05857-118">Сведения, используемые для настройки кнопки на вкладке "Интернет-магазины", такие как текст кнопки и всплывающая подсказка для кнопки.</span><span class="sxs-lookup"><span data-stu-id="05857-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="05857-119">URL-адреса изображений, которые проигрыватель Windows Media отображает для обнаружения интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="05857-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="05857-120">URL-адреса веб-страниц, предоставляемые Интернет-магазином для размещения проигрывателя Windows Media в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="05857-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="05857-121">После начала разработки Интернет-магазина необходимо предоставить корпорации Майкрософт URL-адрес вашего документа ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="05857-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="05857-122">На этапе разработки Интернет-магазин будет отображаться в проигрывателе Windows Media только в том случае, если задан специальный раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="05857-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="05857-123">После публикации интернет-магазина проигрыватель Windows Media автоматически извлекает документ ServiceInfo из Интернета.</span><span class="sxs-lookup"><span data-stu-id="05857-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="05857-124">Однако в некоторых случаях проигрыватель Windows Media извлекает документ ServiceInfo с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="05857-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="05857-125">Дополнительные сведения см. [в разделе Настройка начального Интернет-магазина](setting-the-initial-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="05857-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="05857-126">Когда проигрыватель Windows Media извлекает документ ServiceInfo из Интернета, он добавляет строку запроса к URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="05857-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="05857-127">Строка запроса содержит параметры, предоставляющие сведения о национальной настройке пользователя и версии проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="05857-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="05857-128">Можно создавать статические или динамические документы ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="05857-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="05857-129">Статический документ ServiceInfo имеет расширение имени XML-файла.</span><span class="sxs-lookup"><span data-stu-id="05857-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="05857-130">Динамический документ ServiceInfo является страницей ASP и имеет расширение имени файла. ASP или. aspx.</span><span class="sxs-lookup"><span data-stu-id="05857-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="05857-131">Не все элементы, доступные для использования в документе ServiceInfo, могут использоваться в каждом Интернет-магазине, а некоторые элементы являются необязательными для всех интернет-магазинов.</span><span class="sxs-lookup"><span data-stu-id="05857-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="05857-132">Сведения о типах Интернет-магазинов, которые можно создать, и о функциях, доступных для каждого типа, см. в статье [Интернет-магазины проигрывателя Windows Media](windows-media-player-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="05857-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05857-133">См. также</span><span class="sxs-lookup"><span data-stu-id="05857-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05857-134">**Сведения о типе 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="05857-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="05857-135">**Динамическое создание документа ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="05857-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="05857-136">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="05857-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="05857-137">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="05857-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




