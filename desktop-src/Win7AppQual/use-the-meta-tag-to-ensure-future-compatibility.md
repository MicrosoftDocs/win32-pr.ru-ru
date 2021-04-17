---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Использование тега meta для обеспечения совместимости в будущем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713207"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="9b122-103">Использование тега meta для обеспечения совместимости в будущем</span><span class="sxs-lookup"><span data-stu-id="9b122-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="9b122-104">Windows Internet Explorer 8 позволяет управлять режимами совместимости документов, позволяя обозревателю отображать веб-страницы таким же образом, как и старые версии браузера.</span><span class="sxs-lookup"><span data-stu-id="9b122-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="9b122-105">Вы также можете выбрать время обновления веб-страницы, в то время как она будет использоваться и правильно работать.</span><span class="sxs-lookup"><span data-stu-id="9b122-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="9b122-106">Установка элемента meta</span><span class="sxs-lookup"><span data-stu-id="9b122-106">Setting the Meta Element</span></span>

<span data-ttu-id="9b122-107">Элемент **meta** включает атрибут **Content** , который позволяет указать режим отображения содержимого для веб-страницы, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9b122-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="9b122-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9b122-108">Value</span></span> | <span data-ttu-id="9b122-109">Режим рендеринга</span><span class="sxs-lookup"><span data-stu-id="9b122-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="9b122-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="9b122-110">IE=9</span></span>  | <span data-ttu-id="9b122-111">Использовать режим отображения стандартов Windows Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="9b122-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="9b122-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="9b122-112">IE=8</span></span>  | <span data-ttu-id="9b122-113">Использовать режим отображения стандартов Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="9b122-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="9b122-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="9b122-114">IE=7</span></span>  | <span data-ttu-id="9b122-115">Использовать режим отображения стандартов Windows Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="9b122-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="9b122-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="9b122-116">IE=5</span></span>  | <span data-ttu-id="9b122-117">Использовать режим отображения стандартов Microsoft Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="9b122-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="9b122-118">Дополнительные сведения о совместимости и заголовке X-UA-Compatible см. в разделе [Определение совместимости документов](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) в библиотеке MSDN.</span><span class="sxs-lookup"><span data-stu-id="9b122-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="9b122-119">В следующем примере кода показано, как принудительно отобразить веб-страницу в режиме Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9b122-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a><span data-ttu-id="9b122-120">Использование заголовка HTTP</span><span class="sxs-lookup"><span data-stu-id="9b122-120">Using an HTTP Header</span></span>

<span data-ttu-id="9b122-121">Многие веб-сайты содержат тысячи (или десятки тысяч) отдельных веб-страниц, поэтому установка элемента **meta** в каждом документе непрактична.</span><span class="sxs-lookup"><span data-stu-id="9b122-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="9b122-122">Если вы хотите задать элемент **meta** для всех страниц или коллекцию страниц, выбранных в папке, можно настроить конфигурацию сервера и добавить метаданные X-UA-Compatible в [заголовок HTTP](/previous-versions/cc817572(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="9b122-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="9b122-123">Для сайтов, которым требуются разные значения **мета** -элементов для страниц на том же сервере, существует несколько средств, которые автоматически создают и вставляют соответствующий элемент **meta** .</span><span class="sxs-lookup"><span data-stu-id="9b122-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="9b122-124">Например, служебная программа [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) из Aggiorno вставляет и удаляет функцию тега совместимости Internet Explorer 8 и может помочь вашему сайту соответствовать определенным стандартам совместимости.</span><span class="sxs-lookup"><span data-stu-id="9b122-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b122-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9b122-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b122-126">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="9b122-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
