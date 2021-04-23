---
description: Во время установки установщик Windows установщик может искать файл во всех фиксированных дисках.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Поиск файла во всех фиксированных дисках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673937"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="1c6e0-103">Поиск файла во всех фиксированных дисках</span><span class="sxs-lookup"><span data-stu-id="1c6e0-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="1c6e0-104">**Поиск файла по всем фиксированным дискам**</span><span class="sxs-lookup"><span data-stu-id="1c6e0-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="1c6e0-105">Введите подпись и имя файла в [таблице сигнатур](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1c6e0-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="1c6e0-106">Оставшиеся поля в этой записи могут иметь значение NULL для поиска любой версии MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="1c6e0-107">[Таблица сигнатур](signature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="1c6e0-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="1c6e0-108">Подпись</span><span class="sxs-lookup"><span data-stu-id="1c6e0-108">Signature</span></span>          | <span data-ttu-id="1c6e0-109">Имя файла</span><span class="sxs-lookup"><span data-stu-id="1c6e0-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="1c6e0-110">аппфиле</span><span class="sxs-lookup"><span data-stu-id="1c6e0-110">AppFile</span></span><br/> | <span data-ttu-id="1c6e0-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="1c6e0-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="1c6e0-112">Введите свойство, устанавливаемое установщиком, если MyApp.exe установлен.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="1c6e0-113">Таблица Аппсеарч</span><span class="sxs-lookup"><span data-stu-id="1c6e0-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="1c6e0-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="1c6e0-114">Property</span></span>         | <span data-ttu-id="1c6e0-115">Подпись</span><span class="sxs-lookup"><span data-stu-id="1c6e0-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="1c6e0-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="1c6e0-116">MYAPP</span></span><br/> | <span data-ttu-id="1c6e0-117">аппфиле</span><span class="sxs-lookup"><span data-stu-id="1c6e0-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="1c6e0-118">Используйте [таблицу дрлокатор](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="1c6e0-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="1c6e0-119">Оставьте поля родительский и путь пустыми, чтобы найти все фиксированные диски пользовательской системы.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="1c6e0-120">Укажите в столбце Depth число уровней подкаталогов для поиска.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="1c6e0-121">Например, для установки значения глубины 0 определяет c: \\MyApp.exe, но не обнаруживает файл с глубиной 2, например: c: \\ Program Files \\ MyApps \\MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="1c6e0-122">Таблица Дрлокатор</span><span class="sxs-lookup"><span data-stu-id="1c6e0-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="1c6e0-123">Подпись</span><span class="sxs-lookup"><span data-stu-id="1c6e0-123">Signature</span></span>          | <span data-ttu-id="1c6e0-124">Parent</span><span class="sxs-lookup"><span data-stu-id="1c6e0-124">Parent</span></span> | <span data-ttu-id="1c6e0-125">Путь</span><span class="sxs-lookup"><span data-stu-id="1c6e0-125">Path</span></span> | <span data-ttu-id="1c6e0-126">Глубина</span><span class="sxs-lookup"><span data-stu-id="1c6e0-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="1c6e0-127">аппфиле</span><span class="sxs-lookup"><span data-stu-id="1c6e0-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="1c6e0-128">3</span><span class="sxs-lookup"><span data-stu-id="1c6e0-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="1c6e0-129">Включите действие Аппсеарч в последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="1c6e0-130">Если установлен MyApp.exe, установщик устанавливает свойство MYAPP в расположение файла.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="1c6e0-131">Если файл установлен, MYAPP оценивается как истинное в условном выражении.</span><span class="sxs-lookup"><span data-stu-id="1c6e0-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




