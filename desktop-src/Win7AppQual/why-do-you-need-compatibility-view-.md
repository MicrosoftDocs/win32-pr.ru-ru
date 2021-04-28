---
description: Зачем нужно представление совместимости?
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Зачем нужно представление совместимости?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9991e9dc0c2edcd66ae6655c094f17b240be985a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113382"
---
# <a name="why-do-you-need-compatibility-view"></a><span data-ttu-id="ea7d3-103">Зачем нужно представление совместимости?</span><span class="sxs-lookup"><span data-stu-id="ea7d3-103">Why Do You Need Compatibility View?</span></span>

<span data-ttu-id="ea7d3-104">Функция представления совместимости соответствует набору правил для правильного отображения содержимого без каких-либо действий пользователя (или администратора), когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-104">The Compatibility View feature follows a set of rules to display content correctly, without any user (or IT administrator) action needed whenever possible.</span></span> <span data-ttu-id="ea7d3-105">Представление совместимости позволяет разработчикам указать браузеру, какой модуль визуализации следует использовать, и предоставить пользователям возможность переопределять режимы выбора и переключения браузера.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-105">Compatibility View enables developers to instruct the browser which rendering engine to use and enables users to override the browser’s choice and switch modes.</span></span> <span data-ttu-id="ea7d3-106">Если разработчик и ИТ-специалист не указывают, какой режим рендеринга использовать, пользователь видит значок "Сломанная страница" в правом конце адресной строки, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-106">If the developer and IT professional do not specify which rendering mode to use, user sees the "broken page" icon at the right end of the address bar, as the following illustration shows.</span></span>

![изображение значка неработающей страницы рядом с адресной строкой](images/iecompatview.png)

<span data-ttu-id="ea7d3-108">Если пользователь щелкает значок, Windows Internet Explorer 8 переключает режимы рендеринга, и страница немедленно перезагружается.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-108">If a user clicks the icon, Windows Internet Explorer 8 switches rendering modes, and the page reloads instantly.</span></span>

<span data-ttu-id="ea7d3-109">Пользователи не всегда видят этот значок.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-109">Users do not always see this icon.</span></span> <span data-ttu-id="ea7d3-110">Это вторичное решение, а не основной механизм обеспечения совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-110">It is a secondary solution instead of the primary application compatibility mechanism.</span></span> <span data-ttu-id="ea7d3-111">Windows Internet Explorer отображает этот значок только в том случае, если изменение в представлении совместимости имеет смысл, например, когда пользователь просматривает страницы стандартного режима.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-111">Windows Internet Explorer displays this icon only when a change into Compatibility View makes sense, such as when a user views standards mode pages.</span></span> <span data-ttu-id="ea7d3-112">Во всех остальных случаях, например при просмотре пользователем страниц в режиме совместимости или просмотре узлов зоны интрасети, значок не отображается.</span><span class="sxs-lookup"><span data-stu-id="ea7d3-112">In all other cases, such as when a user views quirks mode pages or views Intranet Zone sites, the icon does not appear.</span></span> <span data-ttu-id="ea7d3-113">Дополнительные сведения о представлении совместимости и о том, когда отображается значок, см. в разделе [Введение в представление совместимости](/archive/blogs/ie/).</span><span class="sxs-lookup"><span data-stu-id="ea7d3-113">For more information about Compatibility View and when the icon appears, see [Introducing Compatibility View](/archive/blogs/ie/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea7d3-114">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="ea7d3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7d3-115">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="ea7d3-115">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
