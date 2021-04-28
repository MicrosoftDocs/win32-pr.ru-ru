---
description: Что такое представление совместимости?
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: Что такое представление совместимости?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be51f94d560d206c579d74d9407d53541205201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113402"
---
# <a name="what-is-compatibility-view"></a><span data-ttu-id="29083-103">Что такое представление совместимости?</span><span class="sxs-lookup"><span data-stu-id="29083-103">What Is Compatibility View?</span></span>

<span data-ttu-id="29083-104">*Представление совместимости* — это компонент Windows Internet Explorer 8, позволяющий браузеру отображать веб-страницу практически так же, как в Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="29083-104">*Compatibility View* is a feature of Windows Internet Explorer 8 that enables the browser to render a webpage nearly identically to the way that Windows Internet Explorer 7 would render it.</span></span>

<span data-ttu-id="29083-105">В обозревателе Internet Explorer 8 представление совместимости изменяет, как браузер интерпретирует код, написанный на CSS, HTML и модель DOM (DOM), чтобы попытаться сопоставить Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="29083-105">In Internet Explorer 8, Compatibility View changes how the browser interprets code that is written in CSS, HTML, and the Document Object Model (DOM) to try to match Internet Explorer 7.</span></span> <span data-ttu-id="29083-106">Сайт, который пользовательское представление в представлении совместимости Internet Explorer 8 почти идентичен сайту, который пользователь просматривает в Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="29083-106">A site that a user views in Internet Explorer 8 Compatibility View is almost identical to a site that the user views in Internet Explorer 7.</span></span> <span data-ttu-id="29083-107">Однако представление совместимости не влияет на то, как браузер интерпретирует весь код.</span><span class="sxs-lookup"><span data-stu-id="29083-107">However, Compatibility View does not change how the browser interprets all code.</span></span> <span data-ttu-id="29083-108">Например, изменения в Internet Explorer 8 для того, как браузер обрабатывает ActiveX, средство синтаксического анализа, AJAX, JavaScript, сети и безопасность может вызвать проблемы совместимости.</span><span class="sxs-lookup"><span data-stu-id="29083-108">For example, the changes in Internet Explorer 8 for how the browser handles ActiveX, the parser, AJAX, JavaScript, networking, and security might still cause compatibility issues.</span></span> <span data-ttu-id="29083-109">Режим совместимости не изменяет эти поведения.</span><span class="sxs-lookup"><span data-stu-id="29083-109">Compatibility View does not change these behaviors.</span></span>

<span data-ttu-id="29083-110">В корпоративной среде некоторые области менее подвержены риску возникновения проблем совместимости.</span><span class="sxs-lookup"><span data-stu-id="29083-110">In an enterprise environment, some areas have lower risk for compatibility issues.</span></span> <span data-ttu-id="29083-111">Например, веб-сайты в зоне интрасети по умолчанию используют просмотр в режиме совместимости.</span><span class="sxs-lookup"><span data-stu-id="29083-111">For example, Intranet Zone websites use Compatibility View by default.</span></span> <span data-ttu-id="29083-112">Клиентские веб-приложения, которые визуализируются с помощью элемента управления веб-браузера или Вебок (механизм подготовки отчетов Internet Explorer), также имеют низкий риск проблем совместимости, так как Internet Explorer 8 по умолчанию использует режим совместимости для Вебок.</span><span class="sxs-lookup"><span data-stu-id="29083-112">Client web applications that render by using the Web Browser Control, or the WebOC (Internet Explorer rendering engine), also have a low risk for compatibility issues because Internet Explorer 8 defaults to a compatibility mode for the WebOC.</span></span> <span data-ttu-id="29083-113">Однако параметры конфигурации по умолчанию для представления совместимости могут не обеспечивать полную совместимость.</span><span class="sxs-lookup"><span data-stu-id="29083-113">However, the default configuration settings for Compatibility View might not ensure complete compatibility.</span></span> <span data-ttu-id="29083-114">Чтобы определить, совместимо ли веб-сайт или веб-приложение с Internet Explorer 8, следует протестировать веб-сайт или веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="29083-114">To determine if a website or web application is compatible with Internet Explorer 8, you should test the website or web application.</span></span>

<span data-ttu-id="29083-115">Дополнительные сведения о различиях между режимом совместимости Internet Explorer 8 и Internet Explorer 7 см. в [блоге по совместимости сайтов и Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).</span><span class="sxs-lookup"><span data-stu-id="29083-115">For more information about the differences between Internet Explorer 8 Compatibility View and Internet Explorer 7, see the [Site Compatibility and Internet Explorer 8 blog](/archive/blogs/ie/site-compatibility-and-ie8).</span></span> <span data-ttu-id="29083-116">Список проверяемых обновлений до Internet Explorer 8 см. в разделе [набор средств подготовки Internet Explorer 8](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).</span><span class="sxs-lookup"><span data-stu-id="29083-116">For a list of what to check when you upgrade to Internet Explorer 8, see the [Internet Explorer 8 Readiness Toolkit](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).</span></span>

<span data-ttu-id="29083-117">Дополнительные сведения о представлении совместимости см. в [блоге группы разработчиков Internet Explorer](/archive/blogs/ie/).</span><span class="sxs-lookup"><span data-stu-id="29083-117">For more information about Compatibility View, see the [Internet Explorer Team Blog](/archive/blogs/ie/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29083-118">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="29083-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29083-119">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="29083-119">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
