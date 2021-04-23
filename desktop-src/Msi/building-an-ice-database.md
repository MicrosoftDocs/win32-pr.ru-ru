---
description: После выбора соответствующей функции ICEs для проверки разработчик должен объединить пользовательские действия в базу данных ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Создание базы данных ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909044"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="c6750-103">Создание базы данных ICE</span><span class="sxs-lookup"><span data-stu-id="c6750-103">Building an ICE Database</span></span>

<span data-ttu-id="c6750-104">После выбора соответствующей функции [ICEs](internal-consistency-evaluators-ices.md) для проверки разработчик должен объединить пользовательские действия в базу данных Ice.</span><span class="sxs-lookup"><span data-stu-id="c6750-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="c6750-105">CUB-файл — это стандартная база данных MSI, которая содержит только ICEs и их обязательные таблицы.</span><span class="sxs-lookup"><span data-stu-id="c6750-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="c6750-106">Невозможно установить CUB-файл, который используется только для хранения и предоставления доступа к настраиваемым действиям ICE.</span><span class="sxs-lookup"><span data-stu-id="c6750-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="c6750-107">CUB-файл содержит следующие таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="c6750-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="c6750-108">Таблица</span><span class="sxs-lookup"><span data-stu-id="c6750-108">Table</span></span>                                  | <span data-ttu-id="c6750-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c6750-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6750-110">Двоичный</span><span class="sxs-lookup"><span data-stu-id="c6750-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="c6750-111">Файлы скриптов, библиотеки DLL и исполняемые действия ICE, упоминаемые в таблице CustomAction.</span><span class="sxs-lookup"><span data-stu-id="c6750-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="c6750-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c6750-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="c6750-113">Каждая запись в этой таблице соответствует пользовательскому действию ICE, входящему в файл. cub.</span><span class="sxs-lookup"><span data-stu-id="c6750-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="c6750-114">\_ицесекуенце</span><span class="sxs-lookup"><span data-stu-id="c6750-114">\_ICESequence</span></span>                          | <span data-ttu-id="c6750-115">В этой таблице перечислены таможенные действия ICE, содержащиеся в файле. cub в последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="c6750-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="c6750-116">Пользовательские действия ICE, перечисленные в этой таблице, выполняются путем вызова [**мсисекуенце**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)или по отдельности, выполняемого с помощью [**мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span><span class="sxs-lookup"><span data-stu-id="c6750-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="c6750-117">\_Проверка</span><span class="sxs-lookup"><span data-stu-id="c6750-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="c6750-118">Эта таблица содержит записи файла. CUB, которые должны быть объединены в \_ таблицу проверки.</span><span class="sxs-lookup"><span data-stu-id="c6750-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c6750-119">\_Предложения</span><span class="sxs-lookup"><span data-stu-id="c6750-119">\_Special</span></span>                              | <span data-ttu-id="c6750-120">Все специальные таблицы, необходимые для конкретных настраиваемых действий ICE, должны быть добавлены в файл. cub.</span><span class="sxs-lookup"><span data-stu-id="c6750-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="c6750-121">Имена этих таблиц должны содержать символ подчеркивания в начале.</span><span class="sxs-lookup"><span data-stu-id="c6750-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="c6750-122">См. [Пример файла Sample. cub](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="c6750-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6750-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c6750-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6750-124">Сборка ICE</span><span class="sxs-lookup"><span data-stu-id="c6750-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



