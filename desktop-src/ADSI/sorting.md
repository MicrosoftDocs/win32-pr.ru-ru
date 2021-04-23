---
title: Сортировка (ADSI)
description: Клиент может запросить сервер для сортировки результирующего набора.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "105654257"
---
# <a name="sorting-adsi"></a><span data-ttu-id="24115-103">Сортировка (ADSI)</span><span class="sxs-lookup"><span data-stu-id="24115-103">Sorting (ADSI)</span></span>

<span data-ttu-id="24115-104">Клиент может запросить сервер для сортировки результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="24115-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="24115-105">Можно указать:</span><span class="sxs-lookup"><span data-stu-id="24115-105">You can specify:</span></span>

-   <span data-ttu-id="24115-106">Порядок сортировки: можно указать порядок сортировки по возрастанию или по убыванию.</span><span class="sxs-lookup"><span data-stu-id="24115-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="24115-107">Атрибуты сортировки: в строке сортировки можно указать несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="24115-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="24115-108">Например, выполните сортировку по фамилии, а затем — по имени.</span><span class="sxs-lookup"><span data-stu-id="24115-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="24115-109">При указании порядка сортировки следует попытаться использовать один из индексированных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="24115-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="24115-110">В противном случае сервер должен вычислить полный результирующий набор перед отправкой клиенту.</span><span class="sxs-lookup"><span data-stu-id="24115-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="24115-111">Это справедливо, даже если вы запросили страничный поиск и указали размер страницы.</span><span class="sxs-lookup"><span data-stu-id="24115-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="24115-112">Не все серверы каталогов поддерживают сортировку нескольких атрибутов или порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="24115-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 




