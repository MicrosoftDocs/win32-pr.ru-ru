---
description: Строка браузера
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Строка браузера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084182"
---
# <a name="user-agent-string"></a><span data-ttu-id="cb8ac-103">Строка браузера</span><span class="sxs-lookup"><span data-stu-id="cb8ac-103">User Agent String</span></span>

<span data-ttu-id="cb8ac-104">*Строка агента пользователя* содержит сведения об удостоверении браузера.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="cb8ac-105">Строка агента пользователя передается на веб-сервер как заголовок HTTP каждый раз, когда браузер выполняет запрос к веб-серверу.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="cb8ac-106">Вы также можете получить доступ к нему через клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="cb8ac-107">Например, можно отобразить строку агента пользователя, введя следующий URL-адрес в адресную строку Windows Internet Explorer 8: "JavaScript: Alert (Navigator. userAgent)".</span><span class="sxs-lookup"><span data-stu-id="cb8ac-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="cb8ac-108">На следующем рисунке показано типичное результирующее диалоговое окно из Internet Explorer 8, работающее под Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![снимок экрана окна Internet Explorer диаог со строкой агента пользователя](images/useragent-alert.png)

<span data-ttu-id="cb8ac-110">Как правило, строка агента пользователя анализируется специально для подстроки MSIE.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="cb8ac-111">На основе сообщаемой версии браузера логика программирования на стороне клиента или на стороне сервера выполняет другое действие.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="cb8ac-112">Дополнительные сведения о строке агента пользователя см. в разделе [что будет отображаться в отчете Windows Internet Explorer как строка User-Agent?](/previous-versions/cc817582(v=msdn.10)) в библиотеке MSDN.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb8ac-113">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="cb8ac-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb8ac-114">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="cb8ac-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



