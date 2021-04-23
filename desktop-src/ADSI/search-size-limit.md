---
title: Ограничение размера поиска
description: Чтобы уменьшить требования к памяти, клиент может сосредоточиться на небольшом количестве объектов, возвращаемых с сервера, и игнорировать оставшуюся часть результирующего набора.
ms.assetid: 675a4931-dfa4-4948-936b-dee27add530c
ms.tgt_platform: multiple
keywords:
- Ограничение размера поиска ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd11148f9e887df1e15e221e8188f9e9e3b10d33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986090"
---
# <a name="search-size-limit"></a><span data-ttu-id="a4761-104">Ограничение размера поиска</span><span class="sxs-lookup"><span data-stu-id="a4761-104">Search Size Limit</span></span>

<span data-ttu-id="a4761-105">Чтобы уменьшить требования к памяти, клиент может сосредоточиться на небольшом количестве объектов, возвращаемых с сервера, и игнорировать оставшуюся часть результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="a4761-105">To reduce memory requirements, a client can focus on a small number of objects returned from the server and ignore the rest of the result set.</span></span> <span data-ttu-id="a4761-106">Для этого клиент указывает предельный размер поиска и другие соответствующие условия поиска.</span><span class="sxs-lookup"><span data-stu-id="a4761-106">To accomplish this, the client specifies a search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="a4761-107">Например, если в каталоге хранятся результаты тестирования учебного района, можно запросить Десять ведущих учащихся с самыми высокими показателями тестирования, указав предельный размер в десять и убывающий порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="a4761-107">For example, if a directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten and a descending sort order.</span></span>

<span data-ttu-id="a4761-108">Дополнительные сведения об использовании параметра предельный размер для поиска с конкретным интерфейсом поиска см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="a4761-108">For more information about using the search size limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="a4761-109">Ограничение размера с IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4761-109">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="a4761-110">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="a4761-110">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="a4761-111">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="a4761-111">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




