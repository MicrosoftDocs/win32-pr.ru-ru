---
description: Компилятор MOF-файл (MOF) поддерживает два стиля комментариев, используя два различных стиля разделителей комментариев.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Создание комментария
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711750"
---
# <a name="creating-a-comment"></a><span data-ttu-id="7b3b4-103">Создание комментария</span><span class="sxs-lookup"><span data-stu-id="7b3b4-103">Creating a Comment</span></span>

<span data-ttu-id="7b3b4-104">Компилятор MOF-файл (MOF) поддерживает два стиля комментариев, используя два различных стиля разделителей комментариев.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="7b3b4-105">В следующей таблице перечислены разделители, используемые для комментариев, и воздействие, которое разделители имеют в коде.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="7b3b4-106">Разделитель</span><span class="sxs-lookup"><span data-stu-id="7b3b4-106">Delimiter</span></span>   | <span data-ttu-id="7b3b4-107">Метки</span><span class="sxs-lookup"><span data-stu-id="7b3b4-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="7b3b4-108">Начало комментария, заканчивающегося в конце строки.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="7b3b4-109">/\* перетаскивани \*/</span><span class="sxs-lookup"><span data-stu-id="7b3b4-109">/\* and \*/</span></span> | <span data-ttu-id="7b3b4-110">Начало и конец комментария, который может охватывать несколько строк или охватывать только часть строки.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="7b3b4-111">Как и в языках программирования C и C++, необходимо использовать разделитель//только с однострочными комментариями, но использовать \* разделители (/и \* /) с однострочными или многострочными комментариями.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="7b3b4-112">В следующем примере кода описываются два стиля разделителей.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="7b3b4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7b3b4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b3b4-114">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



