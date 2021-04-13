---
description: Определяемые пользователем символы (EUDC) в двухбайтовой кодировке (DBCS) и в области частного использования (PUA) в Юникоде — это пользовательские символы.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Символы, определяемые конечным пользователем и частными областями использования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348142"
---
# <a name="end-user-defined-and-private-use-area-characters"></a><span data-ttu-id="39e39-103">Символы, определяемые конечным пользователем и частными областями использования</span><span class="sxs-lookup"><span data-stu-id="39e39-103">End-User-Defined and Private Use Area Characters</span></span>

<span data-ttu-id="39e39-104">Определяемые пользователем символы (EUDC [) в двухбайтовой кодировке](double-byte-character-sets.md) (DBCS) и в области частного использования (PUA) в [Юникоде](unicode.md) — это пользовательские символы.</span><span class="sxs-lookup"><span data-stu-id="39e39-104">End-user-defined characters (EUDC) in [double-byte character sets](double-byte-character-sets.md) (DBCSs) and private use area (PUA) characters in [Unicode](unicode.md) are custom characters.</span></span> <span data-ttu-id="39e39-105">Они могут быть определены и реализованы конечным пользователем или другой стороной, например изготовителем оборудования, группой пользователей, государственным органом или компанией для разработки шрифтов.</span><span class="sxs-lookup"><span data-stu-id="39e39-105">They can be defined and implemented either by an end user or by another party, such as an equipment manufacturer, a user group, a government body, or a font design company.</span></span> <span data-ttu-id="39e39-106">Их использование позволяет пользователям формировать имена и другие слова, используя символы, недоступные в стандартных шрифтах экрана и принтерах.</span><span class="sxs-lookup"><span data-stu-id="39e39-106">Their use enables users to form names and other words using characters that are not available in standard screen and printer fonts.</span></span>

<span data-ttu-id="39e39-107">Символы EUDC и PUA могут быть назначены по-разному или вообще не назначены на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="39e39-107">The EUDC and PUA characters can be assigned differently, or not assigned at all, on different computers.</span></span> <span data-ttu-id="39e39-108">Некоторые кодовые страницы имеют расширения, которые повторно используют диапазон EUDC, и эти расширения могут конфликтовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="39e39-108">Some code pages have extensions that reuse the EUDC range, and these extensions can conflict with each other.</span></span> <span data-ttu-id="39e39-109">В других случаях изготовитель может предоставить пользовательский набор символов в одном из этих диапазонов.</span><span class="sxs-lookup"><span data-stu-id="39e39-109">In other cases, a manufacturer might provide a custom set of characters in one of these ranges.</span></span> <span data-ttu-id="39e39-110">Кроме того, группы пользователей могут попытаться предоставить дополнительные символы в PUA.</span><span class="sxs-lookup"><span data-stu-id="39e39-110">Additionally, user groups can attempt to provide additional characters in the PUA.</span></span> <span data-ttu-id="39e39-111">Различные сочетания этих вариантов могут вызвать конфликт.</span><span class="sxs-lookup"><span data-stu-id="39e39-111">Different combinations of these cases can cause conflict.</span></span> <span data-ttu-id="39e39-112">При создании приложений, зависящих от EUDC или PUA символов, следует помнить о конфликтах интерпретаций отдельной кодовой точки.</span><span class="sxs-lookup"><span data-stu-id="39e39-112">When creating applications that rely on EUDC or PUA characters, you should keep in mind the conflicting interpretations of an individual code point.</span></span>

<span data-ttu-id="39e39-113">В следующих разделах обсуждаются шрифты, поддерживающие Еудкс, а также доступ и управление для этих символов:</span><span class="sxs-lookup"><span data-stu-id="39e39-113">The following topics discuss the fonts that support EUDCs, and access and management for these characters:</span></span>

-   [<span data-ttu-id="39e39-114">Кодировки и шрифты</span><span class="sxs-lookup"><span data-stu-id="39e39-114">Character Sets and Fonts</span></span>](character-sets-and-fonts.md)
-   [<span data-ttu-id="39e39-115">Записи реестра EUDC</span><span class="sxs-lookup"><span data-stu-id="39e39-115">EUDC Registry Entries</span></span>](eudc-registry-entries.md)

## <a name="related-topics"></a><span data-ttu-id="39e39-116">См. также</span><span class="sxs-lookup"><span data-stu-id="39e39-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39e39-117">О кодировке Юникод и кодировке</span><span class="sxs-lookup"><span data-stu-id="39e39-117">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



