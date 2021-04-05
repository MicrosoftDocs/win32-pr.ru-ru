---
title: Использование JavaScript и JScript
description: Использование JavaScript и JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133823"
---
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="fbace-103">Использование JavaScript и JScript</span><span class="sxs-lookup"><span data-stu-id="fbace-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="fbace-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fbace-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fbace-105">Если для доступа к программному интерфейсу Microsoft Agent используется JavaScript или Microsoft JScript, следуйте соглашениям для этого языка, чтобы указать методы или свойства:</span><span class="sxs-lookup"><span data-stu-id="fbace-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="fbace-106">В настоящее время JavaScript не имеет синтаксиса событий для объектов, отличных от HTML.</span><span class="sxs-lookup"><span data-stu-id="fbace-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="fbace-107">Однако в Internet Explorer можно использовать `<SCRIPT>` тег **for... Синтаксис события** :</span><span class="sxs-lookup"><span data-stu-id="fbace-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="fbace-108">Поскольку не все браузеры поддерживают этот синтаксис событий, может потребоваться использовать JavaScript только для страниц, поддерживающих Microsoft Internet Explorer, или для кода, который не требует обработки событий.</span><span class="sxs-lookup"><span data-stu-id="fbace-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="fbace-109">Для доступа к коллекциям объектов агента используйте функцию [**перечислителя**](https://www.bing.com/search?q=**Enumerator**) JScript.</span><span class="sxs-lookup"><span data-stu-id="fbace-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="fbace-110">Однако версии JScript, представленные до Internet Explorer 4,0, не поддерживают эту функцию и не поддерживают коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbace-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="fbace-111">Чтобы получить доступ к методам и свойствам объекта [**character**](/windows/desktop/lwef/the-characters-object) , используйте [**символьный**](character-method.md) метод.</span><span class="sxs-lookup"><span data-stu-id="fbace-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="fbace-112">Аналогично, чтобы получить доступ к свойствам объекта [**Command**](/windows/desktop/lwef/the-command-object) , используйте метод [**Command**](command-method.md) .</span><span class="sxs-lookup"><span data-stu-id="fbace-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 