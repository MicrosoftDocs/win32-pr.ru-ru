---
description: Добавьте запись в таблицу CustomAction для настраиваемого действия запустить.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Добавление запуска в таблицы CustomAction и binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156351"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="77931-103">Добавление запуска в таблицы CustomAction и binary</span><span class="sxs-lookup"><span data-stu-id="77931-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="77931-104">Добавьте запись в [таблицу CustomAction](customaction-table.md) для настраиваемого действия запустить.</span><span class="sxs-lookup"><span data-stu-id="77931-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="77931-105">Введите имя настраиваемого действия в столбце Действие таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="77931-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="77931-106">Введите общий числовой тип для Launch, 65, в столбец Type пользовательской таблицы действий.</span><span class="sxs-lookup"><span data-stu-id="77931-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="77931-107">Исходный столбец таблицы CustomAction задает ключ в записи [двоичной таблицы](binary-table.md) , содержащей двоичные данные для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="77931-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="77931-108">Введите Tutorial.dll в столбец Source таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="77931-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="77931-109">Точка входа, указанная в целевом поле таблицы CustomAction, должна совпадать со значением, экспортированным из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="77931-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="77931-110">Введите Лаунчтуториал в столбец Target таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="77931-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="77931-111">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="77931-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="77931-112">Действие</span><span class="sxs-lookup"><span data-stu-id="77931-112">Action</span></span> | <span data-ttu-id="77931-113">Тип</span><span class="sxs-lookup"><span data-stu-id="77931-113">Type</span></span> | <span data-ttu-id="77931-114">Источник</span><span class="sxs-lookup"><span data-stu-id="77931-114">Source</span></span>       | <span data-ttu-id="77931-115">Назначение</span><span class="sxs-lookup"><span data-stu-id="77931-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="77931-116">Launch</span><span class="sxs-lookup"><span data-stu-id="77931-116">Launch</span></span> | <span data-ttu-id="77931-117">65</span><span class="sxs-lookup"><span data-stu-id="77931-117">65</span></span>   | <span data-ttu-id="77931-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="77931-118">Tutorial.dll</span></span> | <span data-ttu-id="77931-119">лаунчтуториал</span><span class="sxs-lookup"><span data-stu-id="77931-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="77931-120">Добавьте Tutorial.dll, созданные из файла Tutorial. cpp, в двоичный поток в двоичную таблицу.</span><span class="sxs-lookup"><span data-stu-id="77931-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="77931-121">Двоичная таблица</span><span class="sxs-lookup"><span data-stu-id="77931-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="77931-122">Имя</span><span class="sxs-lookup"><span data-stu-id="77931-122">Name</span></span>         | <span data-ttu-id="77931-123">Данные</span><span class="sxs-lookup"><span data-stu-id="77931-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="77931-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="77931-124">Tutorial.dll</span></span> | <span data-ttu-id="77931-125">{*двоичные данные добавлены для библиотеки DLL*}</span><span class="sxs-lookup"><span data-stu-id="77931-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="77931-126">Продолжайте [добавлять события элемента управления в конце установки для запуска запуска](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span><span class="sxs-lookup"><span data-stu-id="77931-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



