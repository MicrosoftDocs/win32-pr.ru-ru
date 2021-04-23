---
title: Функции информации маршрутизатора
description: Используйте следующие функции для работы с заголовками и блоками информации маршрутизатора. Заголовок информации состоит из частных метаданных и информационных блоков. Информационные блоки — это массивы информационных структур различных типов.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067243"
---
# <a name="router-information-functions"></a><span data-ttu-id="56a3c-105">Функции информации маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="56a3c-105">Router Information Functions</span></span>

<span data-ttu-id="56a3c-106">Используйте следующие функции для работы с заголовками и блоками информации маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="56a3c-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="56a3c-107">Заголовок информации состоит из частных метаданных и информационных блоков.</span><span class="sxs-lookup"><span data-stu-id="56a3c-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="56a3c-108">Информационные блоки — это массивы [информационных структур](router-information-structures.md) различных [типов](router-information-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="56a3c-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="56a3c-109">Следующие функции обрабатывают заголовки данных:</span><span class="sxs-lookup"><span data-stu-id="56a3c-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="56a3c-110">**мпринфокреате**</span><span class="sxs-lookup"><span data-stu-id="56a3c-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="56a3c-111">**мпринфоделете**</span><span class="sxs-lookup"><span data-stu-id="56a3c-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="56a3c-112">**мпринфодупликате**</span><span class="sxs-lookup"><span data-stu-id="56a3c-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="56a3c-113">**мпринфоремовеалл**</span><span class="sxs-lookup"><span data-stu-id="56a3c-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="56a3c-114">Следующие функции управляют информационными блоками в заголовке данных:</span><span class="sxs-lookup"><span data-stu-id="56a3c-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="56a3c-115">**мпринфоблоккадд**</span><span class="sxs-lookup"><span data-stu-id="56a3c-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="56a3c-116">**мпринфоблоккфинд**</span><span class="sxs-lookup"><span data-stu-id="56a3c-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="56a3c-117">**мпринфоблокккуерисизе**</span><span class="sxs-lookup"><span data-stu-id="56a3c-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="56a3c-118">**мпринфоблоккремове**</span><span class="sxs-lookup"><span data-stu-id="56a3c-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="56a3c-119">**мпринфоблокксет**</span><span class="sxs-lookup"><span data-stu-id="56a3c-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="56a3c-120">Многие [функции администрирования и настройки маршрутизатора](understanding-mprinfo-functions-and-information-headers.md) используют заголовки данных.</span><span class="sxs-lookup"><span data-stu-id="56a3c-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




