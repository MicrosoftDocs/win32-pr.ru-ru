---
title: Обнаружение проигрывателя
description: Обнаружение проигрывателя
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Интернет-магазины проигрывателя Windows Media, обнаружение игроков
- Интернет-магазины, обнаружение игроков
- Тип 1 Интернет-магазины, обнаружение игроков
- Тип 2 Интернет-магазинов, обнаружение игроков
- Интернет-магазины проигрывателя Windows Media, обнаружение игрока
- Интернет-магазины, обнаружение игроков
- Тип 1 Интернет-магазины, обнаружение игрока
- Тип 2 Интернет-магазинов, обнаружение игрока
- Обнаружение игрока
- Обнаружение игроков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986553"
---
# <a name="detecting-the-player"></a><span data-ttu-id="db2dd-113">Обнаружение проигрывателя</span><span class="sxs-lookup"><span data-stu-id="db2dd-113">Detecting the Player</span></span>

<span data-ttu-id="db2dd-114">При создании веб-страницы для Интернет-магазина вы можете решить, что пользователи должны иметь возможность просматривать страницу в браузере или проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="db2dd-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="db2dd-115">Вы можете использовать сценарий ASP, чтобы определить, размещена ли веб-страница в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="db2dd-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="db2dd-116">Следующий пример кода извлекает параметр version из строки запроса URL-адреса, чтобы определить, размещена ли страница в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="db2dd-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="db2dd-117">Обратите внимание, что в приведенном выше коде предполагается, что параметр version существует в строке запроса при размещении в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="db2dd-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="db2dd-118">Это справедливо для страниц, открытых пользователем, но может быть неверно для страниц, открытых с помощью **External. навигатетаскпанеурл**.</span><span class="sxs-lookup"><span data-stu-id="db2dd-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="db2dd-119">Чтобы строка запроса версии была создана при программном переходе по, необходимо добавить параметр Version в вызов метода или динамически добавить версию к базовому URL-адресу элемента **navigate** в документе serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="db2dd-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db2dd-120">См. также</span><span class="sxs-lookup"><span data-stu-id="db2dd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db2dd-121">**Динамическое создание документа ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="db2dd-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="db2dd-122">**External. Навигатетаскпанеурл**</span><span class="sxs-lookup"><span data-stu-id="db2dd-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="db2dd-123">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="db2dd-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




