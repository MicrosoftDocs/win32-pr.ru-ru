---
description: Во время установки установщик Windows установщик может искать файл в определенном месте в системе пользователя.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Поиск файла в указанном расположении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546023"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="f6f86-103">Поиск файла в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="f6f86-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="f6f86-104">**Поиск файла в определенном месте в пользовательской системе**</span><span class="sxs-lookup"><span data-stu-id="f6f86-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="f6f86-105">Вывод подписи файла и имени в [таблице сигнатур](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6f86-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="f6f86-106">Оставшиеся поля в этой записи могут иметь значение NULL для поиска любой версии MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="f6f86-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="f6f86-107">Таблица сигнатур</span><span class="sxs-lookup"><span data-stu-id="f6f86-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="f6f86-108">Подпись</span><span class="sxs-lookup"><span data-stu-id="f6f86-108">Signature</span></span>          | <span data-ttu-id="f6f86-109">Имя файла</span><span class="sxs-lookup"><span data-stu-id="f6f86-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="f6f86-110">аппфиле</span><span class="sxs-lookup"><span data-stu-id="f6f86-110">AppFile</span></span><br/> | <span data-ttu-id="f6f86-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="f6f86-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="f6f86-112">Введите свойство, устанавливаемое установщиком, если MyApp.exe установлен.</span><span class="sxs-lookup"><span data-stu-id="f6f86-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="f6f86-113">[Таблица аппсеарч](appsearch-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="f6f86-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="f6f86-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="f6f86-114">Property</span></span>         | <span data-ttu-id="f6f86-115">Подпись</span><span class="sxs-lookup"><span data-stu-id="f6f86-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="f6f86-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="f6f86-116">MYAPP</span></span><br/> | <span data-ttu-id="f6f86-117">аппфиле</span><span class="sxs-lookup"><span data-stu-id="f6f86-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="f6f86-118">Используйте [таблицу дрлокатор](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6f86-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="f6f86-119">Введите полный путь к файлу в системе пользователя в поле путь.</span><span class="sxs-lookup"><span data-stu-id="f6f86-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="f6f86-120">Введите значение 0 в столбец Depth для поиска в папке bin.</span><span class="sxs-lookup"><span data-stu-id="f6f86-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="f6f86-121">Таблица Дрлокатор</span><span class="sxs-lookup"><span data-stu-id="f6f86-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="f6f86-122">Подпись</span><span class="sxs-lookup"><span data-stu-id="f6f86-122">Signature</span></span>          | <span data-ttu-id="f6f86-123">Parent</span><span class="sxs-lookup"><span data-stu-id="f6f86-123">Parent</span></span> | <span data-ttu-id="f6f86-124">Путь</span><span class="sxs-lookup"><span data-stu-id="f6f86-124">Path</span></span>                                                    | <span data-ttu-id="f6f86-125">Глубина</span><span class="sxs-lookup"><span data-stu-id="f6f86-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="f6f86-126">аппфиле</span><span class="sxs-lookup"><span data-stu-id="f6f86-126">AppFile</span></span><br/> |        | <span data-ttu-id="f6f86-127">C: \\ Program Files \\ мипродуктс \\ Projects \\ bin</span><span class="sxs-lookup"><span data-stu-id="f6f86-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="f6f86-128">0</span><span class="sxs-lookup"><span data-stu-id="f6f86-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="f6f86-129">Включите действие Аппсеарч в последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="f6f86-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="f6f86-130">Если MyApp.exe установлен в папку C: \\ Program Files \\ мипродуктс \\ Projects \\ , УСТАНОВЩИК устанавливает для свойства MyApp значение Location.</span><span class="sxs-lookup"><span data-stu-id="f6f86-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




