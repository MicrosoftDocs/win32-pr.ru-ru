---
description: Предикат CONTAINS поддерживает использование звездочки ( \* ) в качестве подстановочного знака для представления слов и фраз. Звездочку можно добавить только в конце слова или фразы. Наличие звездочки включает режим сопоставления префикса.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Использование подстановочных знаков в предикате CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144065"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="2e314-105">Использование подстановочных знаков в предикате CONTAINS</span><span class="sxs-lookup"><span data-stu-id="2e314-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="2e314-106">Предикат CONTAINS поддерживает использование звездочки ( \* ) в качестве подстановочного знака для представления слов и фраз.</span><span class="sxs-lookup"><span data-stu-id="2e314-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="2e314-107">Звездочку можно добавить только в конце слова или фразы.</span><span class="sxs-lookup"><span data-stu-id="2e314-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="2e314-108">Наличие звездочки включает режим сопоставления префикса.</span><span class="sxs-lookup"><span data-stu-id="2e314-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="2e314-109">В этом режиме совпадения возвращаются, если столбец содержит указанное слово поиска, за которым следует ноль или более других символов.</span><span class="sxs-lookup"><span data-stu-id="2e314-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="2e314-110">Если указана фраза, совпадения будут обнаружены, если столбец содержит все указанные слова с нулем или более другими символами после последнего слова.</span><span class="sxs-lookup"><span data-stu-id="2e314-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="2e314-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="2e314-111">Examples</span></span>

<span data-ttu-id="2e314-112">Первый пример соответствует документам с любым словом в столбце FileName, начинающимся с «серв».</span><span class="sxs-lookup"><span data-stu-id="2e314-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="2e314-113">Примеры совпадающих слов: "сервер", "серверы" и "служба".</span><span class="sxs-lookup"><span data-stu-id="2e314-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="2e314-114">Во втором примере выполняется сопоставление документов с любой фразой в столбце FileName, которая начинается с "Comp", а следующее слово начинается с "серв".</span><span class="sxs-lookup"><span data-stu-id="2e314-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="2e314-115">Примеры совпадающих слов: "сервер Comp", "серверы Comp" и "служба Comp".</span><span class="sxs-lookup"><span data-stu-id="2e314-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="2e314-116">Звездочка работает только для сопоставления префиксов и может располагаться только в конце слова или фразы; Он не подходит для сопоставления суффикса.</span><span class="sxs-lookup"><span data-stu-id="2e314-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="2e314-117">Следующий синтаксис является недопустимым и не соответствует документам с любым словом в столбце FileName, оканчивающихся на "обслуживает".</span><span class="sxs-lookup"><span data-stu-id="2e314-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="2e314-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2e314-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2e314-119">**Reference**</span><span class="sxs-lookup"><span data-stu-id="2e314-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2e314-120">Предикат FREETEXT</span><span class="sxs-lookup"><span data-stu-id="2e314-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="2e314-121">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="2e314-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



