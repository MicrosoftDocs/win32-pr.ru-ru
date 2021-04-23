---
description: Во время установки установщик Windows установщик может выполнить поиск записи реестра и создать свойство, содержащее значение реестра.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Поиск записи реестра и создание свойства, содержащего значение реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896806"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="42b96-103">Поиск записи реестра и создание свойства, содержащего значение реестра</span><span class="sxs-lookup"><span data-stu-id="42b96-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="42b96-104">**Поиск записи реестра и создание свойства, содержащего значение этого файла**</span><span class="sxs-lookup"><span data-stu-id="42b96-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="42b96-105">Не добавляйте сигнатуру в [таблицу сигнатуры](signature-table.md) или [таблицу комплокатор](complocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="42b96-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="42b96-106">Если подпись файла указана в [таблице аппсеарч](appsearch-table.md) и не указана в таблицах Signature или комплокатор, то установщик выполняет поиск в [таблице реглокатор](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="42b96-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="42b96-107">Укажите запись реестра для поиска в [таблице реглокатор](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="42b96-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="42b96-108">Если подпись отсутствует в [таблице сигнатур](signature-table.md) , а значение столбца Type — **мсидблокатортипераввалуе**, то предполагается, что поиск будет выполняться для конкретного имени раздела реестра, на которое указывает таблица реглокатор.</span><span class="sxs-lookup"><span data-stu-id="42b96-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="42b96-109">[Таблица реглокатор](reglocator-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="42b96-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="42b96-110">Образец\_</span><span class="sxs-lookup"><span data-stu-id="42b96-110">Signature\_</span></span>         | <span data-ttu-id="42b96-111">Root</span><span class="sxs-lookup"><span data-stu-id="42b96-111">Root</span></span>         | <span data-ttu-id="42b96-112">Клавиши</span><span class="sxs-lookup"><span data-stu-id="42b96-112">Key</span></span>                                                           | <span data-ttu-id="42b96-113">Название</span><span class="sxs-lookup"><span data-stu-id="42b96-113">Name</span></span>                  | <span data-ttu-id="42b96-114">Тип</span><span class="sxs-lookup"><span data-stu-id="42b96-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="42b96-115">аппвалуе</span><span class="sxs-lookup"><span data-stu-id="42b96-115">AppValue</span></span><br/> | <span data-ttu-id="42b96-116">2</span><span class="sxs-lookup"><span data-stu-id="42b96-116">2</span></span><br/> | <span data-ttu-id="42b96-117">**Программное обеспечение** \\ **Microsoft** \\ **MyApp**</span><span class="sxs-lookup"><span data-stu-id="42b96-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="42b96-118">**Myname**</span><span class="sxs-lookup"><span data-stu-id="42b96-118">**Myname**</span></span><br/> | <span data-ttu-id="42b96-119">**мсидблокатортипераввалуе**</span><span class="sxs-lookup"><span data-stu-id="42b96-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="42b96-120">Наконец, заполните [таблицу аппсеарч](appsearch-table.md) таким образом, чтобы [действие аппсеарч](appsearch-action.md) возвращало значение аппвалуе.</span><span class="sxs-lookup"><span data-stu-id="42b96-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="42b96-121">После того как установщик выполнит действие Аппсеарч, значение МИРЕГВАЛ будет иметь значение Аппвалуе.</span><span class="sxs-lookup"><span data-stu-id="42b96-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="42b96-122">[Таблица аппсеарч](appsearch-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="42b96-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="42b96-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="42b96-123">Property</span></span>            | <span data-ttu-id="42b96-124">Подпись</span><span class="sxs-lookup"><span data-stu-id="42b96-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="42b96-125">мирегвал</span><span class="sxs-lookup"><span data-stu-id="42b96-125">MYREGVAL</span></span><br/> | <span data-ttu-id="42b96-126">аппвалуе</span><span class="sxs-lookup"><span data-stu-id="42b96-126">AppValue</span></span><br/> |

    

     

 

 




