---
description: В Windows Search используются языковые ресурсы, такие как средство разбиения по словам и парадигматические модули, для разбиения текста в собственном языковом стандарте во время создания индекса и обработки запросов.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Расширение языковых ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710904"
---
# <a name="extending-language-resources"></a><span data-ttu-id="bc9b2-103">Расширение языковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc9b2-103">Extending Language Resources</span></span>

<span data-ttu-id="bc9b2-104">В Windows Search используются языковые ресурсы, такие как средство разбиения по словам и парадигматические модули, для разбиения текста в собственном языковом стандарте во время создания индекса и обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="bc9b2-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="bc9b2-105">Корпорация Майкрософт предоставляет средство разбиения по словам и парадигматические модули для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="bc9b2-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="bc9b2-106">В этом разделе описывается реализация и использование пользовательских средств разбиения по словам и парадигматические модули для языков и национальных настроек, которые выходят за пределы, предоставляемые корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bc9b2-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="bc9b2-107">Основные сведения о компонентах ресурсов языка</span><span class="sxs-lookup"><span data-stu-id="bc9b2-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="bc9b2-108">Реализация средств разбиения по словам и парадигматические модули</span><span class="sxs-lookup"><span data-stu-id="bc9b2-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="bc9b2-109">Рекомендации по лингвистическим правилам и Юникоду</span><span class="sxs-lookup"><span data-stu-id="bc9b2-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="bc9b2-110">Устранение неполадок в языковых ресурсах и рекомендациях</span><span class="sxs-lookup"><span data-stu-id="bc9b2-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="bc9b2-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bc9b2-111">Additional Resources</span></span>

-   <span data-ttu-id="bc9b2-112">Список лануажес, поддерживаемых средством разбиения по словам, см. в разделе [языки, поддерживаемые службой поиска Windows](-search-3x-wds-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="bc9b2-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="bc9b2-113">Если необходимо определить язык фрагмента текста, можно использовать функцию автоматического определения языка (LAD), которая доступна в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="bc9b2-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="bc9b2-114">Дополнительные сведения см. в разделе [Расширенные лингвистические службы](../intl/extended-linguistic-services.md) (ELS).</span><span class="sxs-lookup"><span data-stu-id="bc9b2-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="bc9b2-115">Сведения о применимой справочной документации см. [в разделе интерфейсы надстройки данных](-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="bc9b2-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc9b2-116">См. также</span><span class="sxs-lookup"><span data-stu-id="bc9b2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc9b2-117">Управление индексом</span><span class="sxs-lookup"><span data-stu-id="bc9b2-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="bc9b2-118">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="bc9b2-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="bc9b2-119">Расширение индекса</span><span class="sxs-lookup"><span data-stu-id="bc9b2-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
