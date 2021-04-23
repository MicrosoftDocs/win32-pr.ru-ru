---
description: Чтобы создать модуль слияния, необходимо получить программное средство, с помощью которого можно изменить файл. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Получение средств для создания модулей слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673439"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="1ac36-103">Получение средств для создания модулей слияния</span><span class="sxs-lookup"><span data-stu-id="1ac36-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="1ac36-104">Чтобы создать модуль слияния, необходимо получить программное средство, с помощью которого можно изменить файл. msm.</span><span class="sxs-lookup"><span data-stu-id="1ac36-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="1ac36-105">Поскольку файл. MSM по сути является упрощенным MSI-файлом, вы можете использовать те же средства, что и для создания базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="1ac36-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="1ac36-106">Например, Orca.exe приложений, предоставляемых пакетом SDK для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="1ac36-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="1ac36-107">Альтернативой является приобретение одного из средств упаковки установщика для доступности от независимых поставщиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="1ac36-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="1ac36-108">Существует несколько сторонних средств разработки, которые могут использоваться для создания модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="1ac36-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="1ac36-109">Если вы решили использовать стороннее средство, убедитесь, что он создает модули слияния, которые соответствуют стандарту, описанному в этом документе.</span><span class="sxs-lookup"><span data-stu-id="1ac36-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="1ac36-110">В частности, следует определить, что средства редактирования не выполнили ни одного из следующих действий с модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="1ac36-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="1ac36-111">В модуль слияния добавлены лишние таблицы, на которые нет ссылок в [таблице модулеигноретабле](moduleignoretable-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ac36-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="1ac36-112">Удалите эти таблицы или добавьте их в таблицу Модулеигноретабле.</span><span class="sxs-lookup"><span data-stu-id="1ac36-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="1ac36-113">В модуль слияния добавлена ненужная [Таблица система создала шрифт](textstyle-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1ac36-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="1ac36-114">Если у модуля слияния нет пользовательского интерфейса (и его обычно нет), можно безопасно удалить эту таблицу.</span><span class="sxs-lookup"><span data-stu-id="1ac36-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="1ac36-115">В [таблицу каталога](directory-table.md)добавлены ненужные записи.</span><span class="sxs-lookup"><span data-stu-id="1ac36-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="1ac36-116">Удалите ненужные записи из таблицы Directory.</span><span class="sxs-lookup"><span data-stu-id="1ac36-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="1ac36-117">Левая информация из \_ таблицы проверки модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="1ac36-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="1ac36-118">Это предотвращает проверку модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="1ac36-118">This prevents merge module validation.</span></span> <span data-ttu-id="1ac36-119">Добавьте полную \_ таблицу проверки.</span><span class="sxs-lookup"><span data-stu-id="1ac36-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ac36-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1ac36-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac36-121">Создание пользовательских интерфейсов в модулях слияния</span><span class="sxs-lookup"><span data-stu-id="1ac36-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="1ac36-122">Создание таблиц каталога для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="1ac36-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="1ac36-123">Проверка модулей слияния</span><span class="sxs-lookup"><span data-stu-id="1ac36-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



