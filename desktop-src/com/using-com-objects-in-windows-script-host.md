---
title: Использование COM-объектов в сервере сценариев Windows
description: Сервер сценариев Microsoft Windows — это служебная программа для работы со скриптами, которую можно использовать для выполнения скриптов в базовой операционной системе.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820469"
---
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="c4d02-103">Использование COM-объектов в сервере сценариев Windows</span><span class="sxs-lookup"><span data-stu-id="c4d02-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="c4d02-104">Сервер сценариев Microsoft Windows — это служебная программа для работы со скриптами, которую можно использовать для выполнения скриптов в базовой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="c4d02-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="c4d02-105">Сервер сценариев Windows можно использовать для автоматизации общих задач, а также для создания мощных макросов и сценариев входа в систему.</span><span class="sxs-lookup"><span data-stu-id="c4d02-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="c4d02-106">Сервер сценариев Windows поставляется с обработчиками сценариев VBScript и JScript ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c4d02-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="c4d02-107">Другие производители программного обеспечения предоставляют обработчики скриптов ActiveX для таких языков, как Перлскрипт, Пскрипт, Python и др.</span><span class="sxs-lookup"><span data-stu-id="c4d02-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="c4d02-108">Чтобы использовать COM-объект в скрипте, выполняемом сервером сценариев Windows, необходимо сначала создать экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="c4d02-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="c4d02-109">После создания COM-объекта его можно использовать в скриптах.</span><span class="sxs-lookup"><span data-stu-id="c4d02-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="c4d02-110">Сервер сценариев Windows состоит из двух приложений.</span><span class="sxs-lookup"><span data-stu-id="c4d02-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="c4d02-111">Один запускает сценарии с рабочего стола Windows ( `WScript.exe` ), а другой запускает сценарии из командной строки ( `CScript.exe` ).</span><span class="sxs-lookup"><span data-stu-id="c4d02-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="c4d02-112">Чтобы запустить сценарий с рабочего стола, просто дважды щелкните файл сценария.</span><span class="sxs-lookup"><span data-stu-id="c4d02-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="c4d02-113">Файлы скриптов представляют собой текстовые файлы.</span><span class="sxs-lookup"><span data-stu-id="c4d02-113">Script files are text files.</span></span> <span data-ttu-id="c4d02-114">По соглашению файлы VBScript имеют расширение `.vbs` и файлы JScript `.js` .</span><span class="sxs-lookup"><span data-stu-id="c4d02-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="c4d02-115">Чтобы запустить сценарий из командной строки, запустите `Cscript.exe` приложение с командной строкой, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c4d02-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="c4d02-116">где `c:\\sample scripts\\chart.vbs` — путь к файлу, содержащему скрипт.</span><span class="sxs-lookup"><span data-stu-id="c4d02-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="c4d02-117">Вы можете распечатать список параметров, поддерживаемых Cscript.exe, введя следующую командную строку:</span><span class="sxs-lookup"><span data-stu-id="c4d02-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="c4d02-118">Чтобы использовать COM-объект в скрипте, выполняемом сервером сценариев Windows, необходимо сначала создать экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="c4d02-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="c4d02-119">В VBScript это можно сделать, вызвав `CreateObject()` метод.</span><span class="sxs-lookup"><span data-stu-id="c4d02-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="c4d02-120">В JScript один может использовать либо `ActiveXObject` объект, либо `WScript.CreateObject()` метод.</span><span class="sxs-lookup"><span data-stu-id="c4d02-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="c4d02-121">В следующем примере демонстрируется вызов `CreateObject()` с использованием VBScript:</span><span class="sxs-lookup"><span data-stu-id="c4d02-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="c4d02-122">В следующем примере показано создание `ActiveXObject` объекта с помощью JScript:</span><span class="sxs-lookup"><span data-stu-id="c4d02-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="c4d02-123">В качестве альтернативы можно использовать `WScript.CreateObject()` метод внутри JScript:</span><span class="sxs-lookup"><span data-stu-id="c4d02-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="c4d02-124">После создания экземпляра COM-объекта можно написать сценарий, использующий объект, например:</span><span class="sxs-lookup"><span data-stu-id="c4d02-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="c4d02-125">В дополнение к методу CreateObject и объекту Активексобжект, как VBScript, так и JScript предоставляют метод GetObject, возвращающий экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="c4d02-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4d02-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c4d02-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4d02-127">Создание сценариев с помощью COM-объектов</span><span class="sxs-lookup"><span data-stu-id="c4d02-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




