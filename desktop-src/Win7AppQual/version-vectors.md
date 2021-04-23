---
description: Вектор версии обрабатывает условные комментарии на веб-странице HTML. Это значит, что векторы версий позволяют создавать разметку на основе версии браузера.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Векторы версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350545"
---
# <a name="version-vectors"></a><span data-ttu-id="07f29-104">Векторы версий</span><span class="sxs-lookup"><span data-stu-id="07f29-104">Version Vectors</span></span>

<span data-ttu-id="07f29-105">*Вектор версии* обрабатывает условные комментарии на веб-странице HTML.</span><span class="sxs-lookup"><span data-stu-id="07f29-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="07f29-106">Это значит, что векторы версий позволяют создавать разметку на основе версии браузера.</span><span class="sxs-lookup"><span data-stu-id="07f29-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="07f29-107">Рассмотрим следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="07f29-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="07f29-108">В этом случае, если браузер Windows Internet Explorer имеет версию не ниже 5,5, соответствующий абзац отображается на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="07f29-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="07f29-109">Хотя первое условие в этом примере иллюстрирует функцию условных комментариев, эти комментарии обычно не используются для показа разметки, подобной первому условию.</span><span class="sxs-lookup"><span data-stu-id="07f29-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="07f29-110">Вместо этого остальные условные комментарии в предыдущем примере являются наиболее распространенными.</span><span class="sxs-lookup"><span data-stu-id="07f29-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="07f29-111">В этих оставшихся комментариях условные комментарии используют разные таблицы стилей для каждой версии браузера.</span><span class="sxs-lookup"><span data-stu-id="07f29-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="07f29-112">В предыдущем примере кода также проверяется равенство для Microsoft Internet Explorer 6 и Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="07f29-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="07f29-113">Но для Windows Internet Explorer 8 в примере используется оператор ГТЕ (больше или равно).</span><span class="sxs-lookup"><span data-stu-id="07f29-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="07f29-114">Этот оператор помогает проэкспериментировать в будущем примере, чтобы при выпуске новой версии браузера использовалась наиболее соответствующая стандартам версия таблицы стилей (вместо использования неверной таблицы стилей или таблицы стилей).</span><span class="sxs-lookup"><span data-stu-id="07f29-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="07f29-115">Существующие приложения часто не учитывают версию Internet Explorer, предшествующую 7 (или последнюю версию Internet Explorer, для которой создан сайт).</span><span class="sxs-lookup"><span data-stu-id="07f29-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="07f29-116">Дополнительные сведения о векторах версий см. в разделе [векторы версий](/previous-versions/cc817577(v=msdn.10)) в библиотеке MSDN.</span><span class="sxs-lookup"><span data-stu-id="07f29-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07f29-117">См. также</span><span class="sxs-lookup"><span data-stu-id="07f29-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07f29-118">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="07f29-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



