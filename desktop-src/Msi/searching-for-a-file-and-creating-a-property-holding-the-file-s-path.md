---
description: Во время установки установщик Windows установщик может выполнить поиск файла и создать свойство, содержащее путь к файлу.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Поиск файла и создание свойства, содержащего путь к файлу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910683"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="13648-103">Поиск файла и создание свойства, содержащего путь к файлу</span><span class="sxs-lookup"><span data-stu-id="13648-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="13648-104">**Поиск файла и создание свойства, содержащего путь к этому файлу**</span><span class="sxs-lookup"><span data-stu-id="13648-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="13648-105">Сначала выполните поиск файла, указав подпись файла и имя в [таблице сигнатур](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="13648-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="13648-106">Оставшиеся поля этой записи можно оставить пустыми, чтобы указать поиск любой версии MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="13648-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="13648-107">[Таблица сигнатур](signature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="13648-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="13648-108">Подпись</span><span class="sxs-lookup"><span data-stu-id="13648-108">Signature</span></span>          | <span data-ttu-id="13648-109">Имя файла</span><span class="sxs-lookup"><span data-stu-id="13648-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="13648-110">аппфиле</span><span class="sxs-lookup"><span data-stu-id="13648-110">AppFile</span></span><br/> | <span data-ttu-id="13648-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="13648-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="13648-112">Затем укажите путь к файлу, в котором выполняется поиск, в [таблице дрлокатор](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="13648-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="13648-113">Поскольку Аппфолдер не перечислен в [таблице сигнатур](signature-table.md), установщик определяет, что аппфолдер является папкой, а не файлом.</span><span class="sxs-lookup"><span data-stu-id="13648-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="13648-114">Таблица Дрлокатор</span><span class="sxs-lookup"><span data-stu-id="13648-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="13648-115">Подпись</span><span class="sxs-lookup"><span data-stu-id="13648-115">Signature</span></span>            | <span data-ttu-id="13648-116">Parent</span><span class="sxs-lookup"><span data-stu-id="13648-116">Parent</span></span>             | <span data-ttu-id="13648-117">Путь</span><span class="sxs-lookup"><span data-stu-id="13648-117">Path</span></span> | <span data-ttu-id="13648-118">Глубина</span><span class="sxs-lookup"><span data-stu-id="13648-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="13648-119">аппфиле</span><span class="sxs-lookup"><span data-stu-id="13648-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="13648-120">аппфолдер</span><span class="sxs-lookup"><span data-stu-id="13648-120">AppFolder</span></span><br/> | <span data-ttu-id="13648-121">аппфиле</span><span class="sxs-lookup"><span data-stu-id="13648-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="13648-122">Наконец, заполните [таблицу аппсеарч](appsearch-table.md) , чтобы [действие аппсеарч](appsearch-action.md) возвращало путь аппфолдер.</span><span class="sxs-lookup"><span data-stu-id="13648-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="13648-123">После того как установщик выполнит действие Аппсеарч, значение MYFOLDER является полным путем к Аппфолдер.</span><span class="sxs-lookup"><span data-stu-id="13648-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="13648-124">[Таблица аппсеарч](appsearch-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="13648-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="13648-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="13648-125">Property</span></span>            | <span data-ttu-id="13648-126">Подпись</span><span class="sxs-lookup"><span data-stu-id="13648-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="13648-127">MYFOLDER</span><span class="sxs-lookup"><span data-stu-id="13648-127">MYFOLDER</span></span><br/> | <span data-ttu-id="13648-128">аппфолдер</span><span class="sxs-lookup"><span data-stu-id="13648-128">AppFolder</span></span><br/> |

    

     

 

 




