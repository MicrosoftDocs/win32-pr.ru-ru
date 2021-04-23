---
title: Динамическое создание списков воспроизведения метафайлов Windows Media с помощью страниц ASP
description: Динамическое создание списков воспроизведения метафайлов Windows Media с помощью страниц ASP
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Списки воспроизведения метафайлов Windows Media, создание
- списки воспроизведения метафайлов, создание
- списки воспроизведения, создание
- Списки воспроизведения метафайлов Windows Media, динамическое создание
- списки воспроизведения метафайлов, динамическое создание
- списки воспроизведения, динамическое создание
- Списки воспроизведения метафайлов Windows Media, страницы ASP
- списки воспроизведения метафайлов, страницы ASP
- списки воспроизведения, страницы ASP
- Создание списков воспроизведения метафайлов Windows Media
- Динамическое создание списков воспроизведения метафайлов Windows Media
- ASP-страницы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532072"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a><span data-ttu-id="99ca9-115">Динамическое создание списков воспроизведения метафайлов Windows Media с помощью страниц ASP</span><span class="sxs-lookup"><span data-stu-id="99ca9-115">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>

<span data-ttu-id="99ca9-116">Для динамического создания списков воспроизведения на основе сведений, предоставленных пользователями, можно использовать Active Server страниц (ASP или ASP-файлы).</span><span class="sxs-lookup"><span data-stu-id="99ca9-116">You can use Active Server Pages (ASP, or .asp files) to dynamically generate playlists based on information provided by users.</span></span> <span data-ttu-id="99ca9-117">ASP-страница — это динамическая веб-страница, используемая совместно с Microsoft службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="99ca9-117">An ASP page is a dynamic webpage used in conjunction with Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="99ca9-118">ASP — это среда, в которой можно сочетать HTML, сценарии и многократно используемые серверные компоненты ActiveX для создания динамических и мощных веб-решений.</span><span class="sxs-lookup"><span data-stu-id="99ca9-118">ASP is an environment in which you can combine HTML, scripts, and reusable ActiveX server components to create dynamic and powerful Web-based business solutions.</span></span> <span data-ttu-id="99ca9-119">ASP-страницы позволяют использовать сценарии на стороне сервера для IIS с встроенной поддержкой Microsoft Visual Basic Scripting Edition (VBScript) и Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="99ca9-119">ASP pages enable server-side scripting for IIS with native support for both Microsoft Visual Basic Scripting Edition (VBScript) and Microsoft JScript.</span></span> <span data-ttu-id="99ca9-120">В этом обсуждении предполагается, что вы знакомы с ASP и определяете переменные.</span><span class="sxs-lookup"><span data-stu-id="99ca9-120">This discussion assumes that you are familiar with ASP and defining variables.</span></span>

<span data-ttu-id="99ca9-121">Вся информация заголовка должна содержаться в первой строке строки ASP-страницы, возвращаемой проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="99ca9-121">All header information must be contained on the first line of the ASP page string returned to Windows Media Player.</span></span>

<span data-ttu-id="99ca9-122">При использовании страниц ASP для создания списков воспроизведения необходимо указать значения свойств **ContentType** и **Expires** объекта **Response** на странице ASP из-за проблем с задержкой в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="99ca9-122">When you use ASP pages to generate playlists, you must specify values for the **Response** object's **ContentType** and **expires** properties in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="99ca9-123">Значение **Response. ContentType** должно быть допустимым расширением имени файла для метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="99ca9-123">The **Response.ContentType** value must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="99ca9-124">Допустимые значения: WMA, мастика, WMV, ввкс, ASF и ASX.</span><span class="sxs-lookup"><span data-stu-id="99ca9-124">Acceptable values include wma, wax, wmv, wvx, asf, and asx.</span></span>

<span data-ttu-id="99ca9-125">Свойство **Response. Expires** определяет продолжительность времени в секундах, в течение которого проигрыватель Windows Media кэширует файл списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="99ca9-125">The **Response.expires** property specifies the length of time, in seconds, that Windows Media Player caches the playlist file.</span></span> <span data-ttu-id="99ca9-126">При указании нулевого значения проигрыватель Windows Media запрашивает новый список воспроизведения с сервера каждый раз, когда пользователь обновляет страницу.</span><span class="sxs-lookup"><span data-stu-id="99ca9-126">Specifying a value of zero results in Windows Media Player requesting a new playlist from the server each time the user refreshes the page.</span></span>

<span data-ttu-id="99ca9-127">Дополнительные сведения об использовании объекта **Response** на Active Server страницах см. в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="99ca9-127">See the Platform SDK for details about using the **Response** object in Active Server Pages.</span></span>

<span data-ttu-id="99ca9-128">Следующий код является примером страницы ASP, используемой для создания списка воспроизведения метафайла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="99ca9-128">The following code is an example of an ASP page used to generate a Windows Media metafile playlist.</span></span>


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="99ca9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="99ca9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99ca9-130">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="99ca9-130">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




