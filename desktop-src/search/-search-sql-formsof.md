---
description: Термин FORMSOF выполняет поиск совпадений с другими лингвистическими формами слова.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF термин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701391"
---
# <a name="formsof-term"></a><span data-ttu-id="1cd96-103">FORMSOF термин</span><span class="sxs-lookup"><span data-stu-id="1cd96-103">FORMSOF Term</span></span>

<span data-ttu-id="1cd96-104">Термин FORMSOF выполняет поиск совпадений с другими лингвистическими формами слова.</span><span class="sxs-lookup"><span data-stu-id="1cd96-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="1cd96-105">Ниже приведен синтаксис термина FORMSOF:</span><span class="sxs-lookup"><span data-stu-id="1cd96-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="1cd96-106">Тип поколения указывает, как Microsoft Windows Search выбирает альтернативные формы.</span><span class="sxs-lookup"><span data-stu-id="1cd96-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="1cd96-107">Значение **перегиба** выбирает альтернативные формы перегиба для слов Match.</span><span class="sxs-lookup"><span data-stu-id="1cd96-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="1cd96-108">Если слово является глаголом, используются альтернативные времена.</span><span class="sxs-lookup"><span data-stu-id="1cd96-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="1cd96-109">Если слово является существительным, для обнаружения совпадений используются единственные, множественные и многочисловые формы.</span><span class="sxs-lookup"><span data-stu-id="1cd96-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="1cd96-110">Слово Match \_ — это одно или несколько слов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="1cd96-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="1cd96-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="1cd96-111">Examples</span></span>

<span data-ttu-id="1cd96-112">В следующем примере выполняется поиск совпадений для слова «Run».</span><span class="sxs-lookup"><span data-stu-id="1cd96-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="1cd96-113">Этот пример соответствует документам, содержащим "Run", "выполняющемуся" или "Run".</span><span class="sxs-lookup"><span data-stu-id="1cd96-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="1cd96-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1cd96-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1cd96-115">**Reference**</span><span class="sxs-lookup"><span data-stu-id="1cd96-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1cd96-116">Предикат FREETEXT</span><span class="sxs-lookup"><span data-stu-id="1cd96-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="1cd96-117">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="1cd96-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



