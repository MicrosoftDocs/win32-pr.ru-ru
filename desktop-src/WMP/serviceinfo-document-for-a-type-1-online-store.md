---
title: Документ ServiceInfo для Интернет-магазина типа 1
description: Документ ServiceInfo для Интернет-магазина типа 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Интернет-магазины проигрывателя Windows Media, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 1 Интернет-магазины, документ ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068121"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="355ea-107">Документ ServiceInfo для Интернет-магазина типа 1</span><span class="sxs-lookup"><span data-stu-id="355ea-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="355ea-108">Тип 1 Интернет-магазины должны предоставлять Майкрософт URL-адрес XML-документа, описывающего Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="355ea-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="355ea-109">Проигрыватель Windows Media 11 использует этот документ, чтобы определить, как настроить пользовательский интерфейс для размещения интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="355ea-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="355ea-110">Документ ServiceInfo для хранилища типа 1 предоставляет следующие сведения в проигрывателе Windows Media:</span><span class="sxs-lookup"><span data-stu-id="355ea-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="355ea-111">Сведения, используемые для настройки кнопки **Интернет-магазинов** (также называемой вкладкой), например текст кнопки, цвет кнопки и всплывающая подсказка для кнопки.</span><span class="sxs-lookup"><span data-stu-id="355ea-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="355ea-112">URL-адреса изображений, которые проигрыватель Windows Media отображает для обнаружения интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="355ea-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="355ea-113">URL-адреса веб-страниц, предоставляемые Интернет-магазином для размещения проигрывателя Windows Media в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="355ea-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="355ea-114">URL-адрес, по которому проигрыватель Windows Media может получить подключаемый модуль интернет-магазина, чтобы можно было установить подключаемый модуль на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="355ea-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="355ea-115">Когда проигрыватель Windows Media извлекает документ ServiceInfo из Интернета, он добавляет строку запроса к URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="355ea-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="355ea-116">Строка запроса содержит параметры, предоставляющие сведения о языковом стандарте пользователя и географическом расположении, а также версию проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="355ea-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="355ea-117">См. также</span><span class="sxs-lookup"><span data-stu-id="355ea-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="355ea-118">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="355ea-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="355ea-119">**Динамическое создание документа ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="355ea-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="355ea-120">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="355ea-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="355ea-121">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="355ea-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




