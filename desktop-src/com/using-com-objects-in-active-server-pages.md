---
title: Использование COM-объектов на страницах Active Server
description: Вы можете создать скрипты COM-объектов в приложениях Active Server Pages (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328635"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="991b9-103">Использование COM-объектов на страницах Active Server</span><span class="sxs-lookup"><span data-stu-id="991b9-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="991b9-104">Вы можете создать скрипты COM-объектов в приложениях Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="991b9-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="991b9-105">Для этого необходимо сначала создать экземпляр объекта с помощью тега OBJECT или путем вызова метода CreateObject объекта сервера ASP.</span><span class="sxs-lookup"><span data-stu-id="991b9-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="991b9-106">После создания COM-объекта его можно использовать в последующих скриптах на странице ASP.</span><span class="sxs-lookup"><span data-stu-id="991b9-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="991b9-107">С помощью ASP можно работать с множеством различных типов обработчиков сценариев, каждый из которых поддерживает различные языки сценариев.</span><span class="sxs-lookup"><span data-stu-id="991b9-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="991b9-108">ASP поставляется с обработчиками сценариев VBScript и JScript.</span><span class="sxs-lookup"><span data-stu-id="991b9-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="991b9-109">Можно также подключать обработчики скриптов, разработанные другими компаниями, для поддержки таких языков, как Перлскрипт, Пскрипт, Python и др.</span><span class="sxs-lookup"><span data-stu-id="991b9-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="991b9-110">Если не задать язык скрипта для страницы ASP, по умолчанию используется VBScript.</span><span class="sxs-lookup"><span data-stu-id="991b9-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="991b9-111">Чтобы указать язык сценариев, отличный от VBScript, включите в начало каждой страницы ASP строку, следующую как:</span><span class="sxs-lookup"><span data-stu-id="991b9-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="991b9-112">Чтобы использовать COM-объект на странице ASP, необходимо сначала создать экземпляр этого объекта.</span><span class="sxs-lookup"><span data-stu-id="991b9-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="991b9-113">Это делается с помощью тега объекта и указания значения "SERVER" для атрибута RUNAT, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="991b9-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="991b9-114">По умолчанию тег объекта создает экземпляр объекта на клиенте.</span><span class="sxs-lookup"><span data-stu-id="991b9-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="991b9-115">Установка для атрибута RUNAT значения SERVER приводит к созданию объекта на сервере.</span><span class="sxs-lookup"><span data-stu-id="991b9-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="991b9-116">Объект должен быть запущен на сервере, чтобы его можно было использовать в ASP.</span><span class="sxs-lookup"><span data-stu-id="991b9-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="991b9-117">Можно также создать экземпляр COM-объекта на странице ASP, вызвав метод CreateObject объекта сервера ASP.</span><span class="sxs-lookup"><span data-stu-id="991b9-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="991b9-118">Использование Server. CreateObject медленнее, чем создание объекта с помощью тега объекта, но он немного более удобочитаем, так как указывает программный идентификатор, а не идентификатор класса COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="991b9-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="991b9-119">Объект сервера предоставляется ASP и не требует создания.</span><span class="sxs-lookup"><span data-stu-id="991b9-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="991b9-120">Способ вызова Server. CreateObject показан в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="991b9-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="991b9-121">Первый пример — VBScript:</span><span class="sxs-lookup"><span data-stu-id="991b9-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="991b9-122">Следующий пример — JScript:</span><span class="sxs-lookup"><span data-stu-id="991b9-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="991b9-123">Вызов функции CreateObject выполняется медленнее, чем использование тега объекта для создания COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="991b9-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="991b9-124">В приложениях, в которых важна производительность, следует использовать тег OBJECT.</span><span class="sxs-lookup"><span data-stu-id="991b9-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="991b9-125">После создания экземпляра COM-объекта его можно использовать в скриптах.</span><span class="sxs-lookup"><span data-stu-id="991b9-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="991b9-126">Это показано в следующем примере сценария VBScript, который задает значение свойства Border объекта COM.</span><span class="sxs-lookup"><span data-stu-id="991b9-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="991b9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="991b9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="991b9-128">Создание сценариев с помощью COM-объектов</span><span class="sxs-lookup"><span data-stu-id="991b9-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




