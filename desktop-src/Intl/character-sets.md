---
description: '&\# 0034, набор символов&\# 0034; — это сопоставление символов с их кодовыми значениями.'
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Кодировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682628"
---
# <a name="character-sets"></a><span data-ttu-id="6e470-103">Кодировки</span><span class="sxs-lookup"><span data-stu-id="6e470-103">Character Sets</span></span>

<span data-ttu-id="6e470-104">"Набор символов" — это сопоставление символов с их кодовыми значениями.</span><span class="sxs-lookup"><span data-stu-id="6e470-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="6e470-105">Чаще всего в настоящее время для компьютеров используется [Юникод](unicode.md), глобальный стандарт для кодировки символов.</span><span class="sxs-lookup"><span data-stu-id="6e470-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="6e470-106">На внутреннем уровне в приложениях Windows используется реализация Юникода в кодировке UTF-16.</span><span class="sxs-lookup"><span data-stu-id="6e470-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="6e470-107">В UTF-16 большинство символов идентифицируются с помощью двухбайтовых кодов.</span><span class="sxs-lookup"><span data-stu-id="6e470-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="6e470-108">Менее часто используемые добавочные символы представлены парой символов-заместителей, которая представляет собой пару из двух байтовых кодов.</span><span class="sxs-lookup"><span data-stu-id="6e470-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="6e470-109">Дополнительные сведения см. в разделе [суррогаты и добавочные символы](surrogates-and-supplementary-characters.md).</span><span class="sxs-lookup"><span data-stu-id="6e470-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="6e470-110">Некоторые приложения Windows должны работать с более старыми наборами символов, собственными для Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="6e470-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="6e470-111">[Кодовые страницы Windows](code-pages.md) позволяют приложению работать с этими наборами символов.</span><span class="sxs-lookup"><span data-stu-id="6e470-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="6e470-112">Эти наборы символов можно разделить на следующие:</span><span class="sxs-lookup"><span data-stu-id="6e470-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="6e470-113">[Однобайтовые кодировки](single-byte-character-sets.md) (SBCS).</span><span class="sxs-lookup"><span data-stu-id="6e470-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="6e470-114">В SBCS каждый символ идентифицируется по значению на один байт.</span><span class="sxs-lookup"><span data-stu-id="6e470-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="6e470-115">Многобайтовые наборы символов, в частности [двухбайтовые](double-byte-character-sets.md) кодировки (DBCS).</span><span class="sxs-lookup"><span data-stu-id="6e470-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="6e470-116">Многобайтовые кодировки предоставляют средства для представления большого количества символов на многих азиатских языках.</span><span class="sxs-lookup"><span data-stu-id="6e470-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="6e470-117">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6e470-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6e470-118">Кодовые страницы</span><span class="sxs-lookup"><span data-stu-id="6e470-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="6e470-119">Двухбайтовые кодировки</span><span class="sxs-lookup"><span data-stu-id="6e470-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="6e470-120">Однобайтовые кодировки</span><span class="sxs-lookup"><span data-stu-id="6e470-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="6e470-121">Суррогаты и дополнительные символы</span><span class="sxs-lookup"><span data-stu-id="6e470-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="6e470-122">Юникод</span><span class="sxs-lookup"><span data-stu-id="6e470-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="6e470-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6e470-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e470-124">О кодировке Юникод и кодировке</span><span class="sxs-lookup"><span data-stu-id="6e470-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



