---
title: Внедрение объектов COM в веб-страницы
description: На веб-страницах можно использовать COM-объекты. Для этого сначала создайте экземпляр этого COM-объекта. После создания экземпляра объекта его можно использовать в последующих сценариях на этой веб-странице.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329376"
---
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="ff60d-105">Внедрение объектов COM в веб-страницы</span><span class="sxs-lookup"><span data-stu-id="ff60d-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="ff60d-106">На веб-страницах можно использовать COM-объекты.</span><span class="sxs-lookup"><span data-stu-id="ff60d-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="ff60d-107">Для этого сначала создайте экземпляр этого COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="ff60d-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="ff60d-108">После создания экземпляра объекта его можно использовать в последующих сценариях на этой веб-странице.</span><span class="sxs-lookup"><span data-stu-id="ff60d-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="ff60d-109">Чтобы создать экземпляр COM-объекта на веб-странице, можно использовать тег объекта.</span><span class="sxs-lookup"><span data-stu-id="ff60d-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="ff60d-110">Кроме того, если ваш язык сценариев предоставляет собственный способ создания COM-объектов, можно создать экземпляр объекта с помощью скрипта.</span><span class="sxs-lookup"><span data-stu-id="ff60d-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="ff60d-111">Обратите внимание, что внедрение COM-объектов на веб-страницах работает только в браузерах, поддерживающих ActiveX и COM, например Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ff60d-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="ff60d-112">В следующем примере показано использование тега OBJECT для внедрения COM-объекта на веб-страницу:</span><span class="sxs-lookup"><span data-stu-id="ff60d-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

<span data-ttu-id="ff60d-113">Можно также создать экземпляр COM-объекта в скрипте, если ваш язык сценариев предоставляет способ создания COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="ff60d-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="ff60d-114">Например, VBScript предоставляет метод CreateObject, а JScript предоставляет объект Активексобжект.</span><span class="sxs-lookup"><span data-stu-id="ff60d-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="ff60d-115">Создание объектов в сценарии показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="ff60d-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="ff60d-116">В дополнение к методу CreateObject и объекту Активексобжект, как VBScript, так и JScript предоставляют метод GetObject, возвращающий экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="ff60d-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="ff60d-117">После создания COM-объекта его можно сослать на него в последующих скриптах, используя идентификатор, указанный в атрибуте ID тега объекта.</span><span class="sxs-lookup"><span data-stu-id="ff60d-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="ff60d-118">В предыдущем примере этот идентификатор был указан как "VID".</span><span class="sxs-lookup"><span data-stu-id="ff60d-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="ff60d-119">Обратите внимание, что скрипт, использующий COM-объект, должен появиться после тега объекта или скрипта, который создает экземпляр объекта. в противном случае идентификатор объекта не определен.</span><span class="sxs-lookup"><span data-stu-id="ff60d-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="ff60d-120">Следующий скрипт использует объект Обжксл для вывода сведений о версии для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ff60d-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="ff60d-121">При написании скриптов, внедренных на веб-страницу, браузер также предоставляет объектную модель, к которой могут обращаться ваши скрипты.</span><span class="sxs-lookup"><span data-stu-id="ff60d-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="ff60d-122">Модель, используемая Internet Explorer, соответствует модель DOM (DOM), предложенной консорциум W3C (W3C).</span><span class="sxs-lookup"><span data-stu-id="ff60d-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff60d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ff60d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff60d-124">Создание сценариев с помощью COM-объектов</span><span class="sxs-lookup"><span data-stu-id="ff60d-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




