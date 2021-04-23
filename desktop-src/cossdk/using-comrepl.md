---
description: Использование COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Использование COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807630"
---
# <a name="using-comrepl"></a><span data-ttu-id="44ba5-103">Использование COMREPL</span><span class="sxs-lookup"><span data-stu-id="44ba5-103">Using COMREPL</span></span>

<span data-ttu-id="44ba5-104">Чтобы запустить программу командной строки COMREPL, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="44ba5-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="44ba5-105">Добавьте% WINDIR% \\ system32 \\ com в путь среды по умолчанию, введя в командной строке следующее:</span><span class="sxs-lookup"><span data-stu-id="44ba5-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="44ba5-106">**Set путь =% PATH%;% WINDIR% \\ system32 \\ com**</span><span class="sxs-lookup"><span data-stu-id="44ba5-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="44ba5-107">Введите следующую команду COMREPL:</span><span class="sxs-lookup"><span data-stu-id="44ba5-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="44ba5-108">**COMREPL** *саурцекомпутер* *таржеткомпутерлист* **\[ \[ /n \] /v \]**</span><span class="sxs-lookup"><span data-stu-id="44ba5-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="44ba5-109">где:</span><span class="sxs-lookup"><span data-stu-id="44ba5-109">where:</span></span>

    -   <span data-ttu-id="44ba5-110">*саурцекомпутер* — имя компьютера источника.</span><span class="sxs-lookup"><span data-stu-id="44ba5-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="44ba5-111">*таржеткомпутерлист* — имена компьютеров, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="44ba5-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="44ba5-112">**/n** вывод запроса на подтверждение перед запуском репликации</span><span class="sxs-lookup"><span data-stu-id="44ba5-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="44ba5-113">**/v** вывод выходных данных файла журнала на консоль</span><span class="sxs-lookup"><span data-stu-id="44ba5-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="44ba5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="44ba5-114">Notes</span></span>

-   <span data-ttu-id="44ba5-115">Поскольку COM+ не реплицируется (только данные конфигурации и приложения), на всех целевых компьютерах уже должен быть установлен COM+.</span><span class="sxs-lookup"><span data-stu-id="44ba5-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="44ba5-116">Пользователь должен передать проверки роли для системного приложения как на исходном, так и на целевом компьютерах.</span><span class="sxs-lookup"><span data-stu-id="44ba5-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="44ba5-117">Не реплицируются учетные записи локального компьютера, которые могут использоваться ролями.</span><span class="sxs-lookup"><span data-stu-id="44ba5-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="44ba5-118">Целевые компьютеры должны быть подключены к сети.</span><span class="sxs-lookup"><span data-stu-id="44ba5-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="44ba5-119">Пользователь несет ответственность за репликацию всех данных, отличных от COM + (например, таблиц базы данных, файлов данных и т. д.) на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="44ba5-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="44ba5-120">Кластеры могут участвовать в репликации, но обратите внимание, что COMREPL реплицируется только на компьютеры с именованными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="44ba5-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44ba5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="44ba5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44ba5-122">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="44ba5-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="44ba5-123">Ведение журнала и отчеты об ошибках</span><span class="sxs-lookup"><span data-stu-id="44ba5-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="44ba5-124">Этапы репликации</span><span class="sxs-lookup"><span data-stu-id="44ba5-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="44ba5-125">Что реплицируется</span><span class="sxs-lookup"><span data-stu-id="44ba5-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



