---
description: ICE29 проверяет, что усеченные имена потоков остаются уникальными. Проверяется любая таблица, в которой находится двоичный или столбец объекта. См. тип данных в двоичном столбце.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991579"
---
# <a name="ice29"></a><span data-ttu-id="a9f0a-105">ICE29</span><span class="sxs-lookup"><span data-stu-id="a9f0a-105">ICE29</span></span>

<span data-ttu-id="a9f0a-106">ICE29 проверяет, что усеченные имена потоков остаются уникальными.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-106">ICE29 validates that truncated stream names remain unique.</span></span> <span data-ttu-id="a9f0a-107">Проверяется любая таблица, в которой находится двоичный или столбец объекта.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-107">Any table having a Binary or Object column is validated.</span></span> <span data-ttu-id="a9f0a-108">См. тип данных в [двоичном](binary.md) столбце.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-108">See the [Binary](binary.md) column data type.</span></span>

<span data-ttu-id="a9f0a-109">Обработка потоков с помощью реализации структурированного хранилища Win32 OLE ограничивает имена потоков.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-109">Handling of streams by the Win32 OLE structured storage implementation limits stream names.</span></span> <span data-ttu-id="a9f0a-110">См. раздел [ограничения OLE для потоков](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="a9f0a-110">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="a9f0a-111">Установщик может сжимать имена потоков длиной до 62 символов.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-111">The installer can compress stream names up to 62 characters in length.</span></span> <span data-ttu-id="a9f0a-112">Имена, превышающие это, усекаются.</span><span class="sxs-lookup"><span data-stu-id="a9f0a-112">Names longer than this are truncated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9f0a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a9f0a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f0a-114">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="a9f0a-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



