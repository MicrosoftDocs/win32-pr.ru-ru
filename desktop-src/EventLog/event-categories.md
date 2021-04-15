---
description: Категории помогают упорядочить события, чтобы Просмотр событий можно было отфильтровать их. Каждый источник событий может определять собственные нумерованные категории и текстовые строки, с которыми они сопоставляются.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Категории событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682956"
---
# <a name="event-categories"></a><span data-ttu-id="89927-104">Категории событий</span><span class="sxs-lookup"><span data-stu-id="89927-104">Event Categories</span></span>

<span data-ttu-id="89927-105">Категории помогают упорядочить события, чтобы Просмотр событий можно было отфильтровать их.</span><span class="sxs-lookup"><span data-stu-id="89927-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="89927-106">Каждый [источник событий](event-sources.md) может определять собственные нумерованные категории и текстовые строки, с которыми они сопоставляются.</span><span class="sxs-lookup"><span data-stu-id="89927-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="89927-107">Категории должны быть пронумерованы последовательно, начиная с номера 1.</span><span class="sxs-lookup"><span data-stu-id="89927-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="89927-108">Сами категории определяются в файле сообщения.</span><span class="sxs-lookup"><span data-stu-id="89927-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="89927-109">Например, используйте следующий синтаксис для объявления трех категорий событий.</span><span class="sxs-lookup"><span data-stu-id="89927-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="89927-110">В Просмотр событий события, которые используют эти категории, будут иметь категорию 1, Категория 2 или категорию 3, отображенные в столбце **Категория** .</span><span class="sxs-lookup"><span data-stu-id="89927-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

<span data-ttu-id="89927-111">Категории могут храниться в отдельном файле сообщений или в файле, содержащем сообщения других типов.</span><span class="sxs-lookup"><span data-stu-id="89927-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="89927-112">Если создается один файл сообщения, убедитесь, что эти категории являются первыми сообщениями в файле.</span><span class="sxs-lookup"><span data-stu-id="89927-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="89927-113">Дополнительные сведения о создании и использовании файлов сообщений см. в разделе [файлы сообщений](message-files.md).</span><span class="sxs-lookup"><span data-stu-id="89927-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="89927-114">Общее число категорий хранится в значении **категорикаунт** для источника события.</span><span class="sxs-lookup"><span data-stu-id="89927-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 



