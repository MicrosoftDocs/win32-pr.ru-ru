---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: Нотация объектов JavaScript (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265005"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="24c9f-103">Нотация объектов JavaScript (JSON)</span><span class="sxs-lookup"><span data-stu-id="24c9f-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="24c9f-104">[Нотация объектов JavaScript (JSON)](https://www.json.org/) — это простой и упрощенный формат обмена данными, основанный на подмножестве нотации объектного литерала языка JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24c9f-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="24c9f-105">Подсистема JavaScript в Windows Internet Explorer 8 реализует [предложение ECMAScript 3,1 JSON](https://www.ecma-international.org/) для собственных функций обработки JSON (которые используют [json2.js API-интерфейс Дугласа Крокфорда](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span><span class="sxs-lookup"><span data-stu-id="24c9f-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="24c9f-106">Internet Explorer 8 включает собственный объект JSON, который соответствует поддержке JSON, описанной в [рабочем черновике предложения ES 3.1](https://www.ecma-international.org/).</span><span class="sxs-lookup"><span data-stu-id="24c9f-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="24c9f-107">Некоторые веб-страницы обнаруживают собственный объект JSON, а затем используют его нестандартным способом.</span><span class="sxs-lookup"><span data-stu-id="24c9f-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="24c9f-108">Такое использование обычно вызывает ошибку сценария и прерывает обработку запросов AJAX.</span><span class="sxs-lookup"><span data-stu-id="24c9f-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="24c9f-109">В следующем примере кода показан неправильный способ использования объекта JSON.</span><span class="sxs-lookup"><span data-stu-id="24c9f-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="24c9f-110">Вместо этого в следующем примере кода демонстрируется хороший способ использования объекта JSON.</span><span class="sxs-lookup"><span data-stu-id="24c9f-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="24c9f-111">Windows Internet Explorer содержит встроенную поддержку JSON, представляя глобальный объект JSON с двумя встроенными методами: **stringify** и **Parse**.</span><span class="sxs-lookup"><span data-stu-id="24c9f-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="24c9f-112">Глобальный объект JSON определяется в подсистеме JavaScript и создается на этапе инициализации подсистемы.</span><span class="sxs-lookup"><span data-stu-id="24c9f-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="24c9f-113">Для обеспечения обратной совместимости эта функция доступна, только если на веб-сайте используется последняя версия функций JavaScript с использованием режима макета "Internet Explorer 8 Standards" (документ).</span><span class="sxs-lookup"><span data-stu-id="24c9f-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="24c9f-114">Эта функция также может повлиять на поведение веб-страниц, зависящих от глобальной переменной JSON, или использовать [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span><span class="sxs-lookup"><span data-stu-id="24c9f-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="24c9f-115">Можно переопределить глобальный объект JSON.</span><span class="sxs-lookup"><span data-stu-id="24c9f-115">You can override the global JSON object.</span></span> <span data-ttu-id="24c9f-116">Но если веб-страница использует режим макета "Internet Explorer 8 Standards" (документ), он больше не является неопределенным объектом.</span><span class="sxs-lookup"><span data-stu-id="24c9f-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="24c9f-117">Так как модуль JavaScript создает экземпляр JSON в качестве глобального имени, он возвращает значение false, например "if (! this.JSON)", и в пользовательском коде его необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="24c9f-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="24c9f-118">Веб-страницы, использующие [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) , скорее всего, не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="24c9f-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="24c9f-119">С некоторыми исключениями эти страницы должны работать быстрее.</span><span class="sxs-lookup"><span data-stu-id="24c9f-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="24c9f-120">Исключения вызваны различиями в реализации собственного JSON и json2.js в обозревателе Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="24c9f-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="24c9f-121">Например, во время сериализации собственная реализация JSON обнаруживает циклы и не переходит в бесконечную рекурсию, например json.js.</span><span class="sxs-lookup"><span data-stu-id="24c9f-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="24c9f-122">Дополнительные сведения об этих исключениях см. в [блогах по JavaScript](/archive/blogs/jscript/).</span><span class="sxs-lookup"><span data-stu-id="24c9f-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="24c9f-123">Дополнительные сведения см. в статьях [Документация по JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) , [Управление версиями и поддержка версий модуля JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span><span class="sxs-lookup"><span data-stu-id="24c9f-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24c9f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="24c9f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c9f-125">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="24c9f-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
