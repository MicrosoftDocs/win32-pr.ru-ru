---
description: Важно для Организации того, какие файлы какого модуля записи следует архивировать или восстанавливать, является понятием компонента.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Компоненты метаданных VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692372"
---
# <a name="vss-metadata-components"></a><span data-ttu-id="c64b6-103">Компоненты метаданных VSS</span><span class="sxs-lookup"><span data-stu-id="c64b6-103">VSS Metadata Components</span></span>

<span data-ttu-id="c64b6-104">Важно для Организации того, какие файлы какого модуля записи следует архивировать или восстанавливать, является понятием [*компонента*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="c64b6-104">Critical to organizing which files of which writer are to be backed up or restored is the concept of a [*component*](vssgloss-c.md).</span></span>

<span data-ttu-id="c64b6-105">Компоненты позволяют модулю записи указать подсистеме резервного копирования, каким способом следует организовывать файлы, зависимости между файлами и тип данных, которые могут содержать эти файлы.</span><span class="sxs-lookup"><span data-stu-id="c64b6-105">Components allow a writer to indicate to a backup engine how its files are to be organized, dependencies between files, and what type of data those files can contain.</span></span> <span data-ttu-id="c64b6-106">Это позволяет механизму резервного копирования выбрать способ хранения файлов для максимальной эффективности.</span><span class="sxs-lookup"><span data-stu-id="c64b6-106">This allows a backup engine to decide how to store files for maximum efficiency.</span></span>

<span data-ttu-id="c64b6-107">Кроме того, приложения на основе VSS используют компоненты в качестве стандартных блоков для их метаданных, а также носитель для обмена данными между модулем записи и запрашивающей стороны.</span><span class="sxs-lookup"><span data-stu-id="c64b6-107">In addition, VSS-based applications use components as the building blocks for their metadata and the medium for writer/requester communication.</span></span>

<span data-ttu-id="c64b6-108">Модули записи и запрашивающие хранят сведения о компонентах отдельно — в документе метаданных модуля записи и в документе компонентов резервного копирования соответственно, а сведения в каждом представлении различаются.</span><span class="sxs-lookup"><span data-stu-id="c64b6-108">Writers and requesters store information about components separately—in the Writer Metadata Document and the Backup Components Document, respectively—and the information differs in each representation.</span></span>

<span data-ttu-id="c64b6-109">Сведения о компоненте в документах метаданных модуля записи включают в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="c64b6-109">Component information in Writer Metadata Documents includes the following:</span></span>

-   <span data-ttu-id="c64b6-110">Информация только от одного модуля записи в каждом документе</span><span class="sxs-lookup"><span data-stu-id="c64b6-110">Information from only one writer in each document</span></span>
-   <span data-ttu-id="c64b6-111">Все компоненты этого модуля записи, могут ли они быть [*явно добавлены*](vssgloss-e.md) или должны быть [*неявно добавлены*](vssgloss-i.md) в операцию резервного копирования или восстановления</span><span class="sxs-lookup"><span data-stu-id="c64b6-111">All of that writer's components, whether they can be [*explicitly included*](vssgloss-e.md) or must be [*implicitly included*](vssgloss-i.md) in a backup or restore operation</span></span>
-   <span data-ttu-id="c64b6-112">Сведения о [*логическом пути*](vssgloss-l.md) , используемые для связывания компонента резервного копирования, который можно выбрать, с определенным невыбираемым для компонентов резервного копирования, тем самым формируя набор компонентов.</span><span class="sxs-lookup"><span data-stu-id="c64b6-112">[*Logical path*](vssgloss-l.md) information used to associate a selectable for backup component with particular nonselectable for backup components, thus forming a component set</span></span>
-   <span data-ttu-id="c64b6-113">Сведения о [*наборе файлов*](vssgloss-f.md) — путь, спецификация файла и флаг рекурсии — управляются для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="c64b6-113">The [*file set*](vssgloss-f.md) information—path, file specification, and recursion flag—managed for each component</span></span>

<span data-ttu-id="c64b6-114">Документы метаданных модуля записи также содержат сведения о метаданных уровня записи, такие как методы восстановления и сопоставления альтернативного расположения для восстановления.</span><span class="sxs-lookup"><span data-stu-id="c64b6-114">Writer Metadata Documents also contain writer-level metadata information, such as restore methods and alternate location mappings for restore.</span></span> <span data-ttu-id="c64b6-115">Документы метаданных модуля записи доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c64b6-115">Writer Metadata Documents are read-only.</span></span> <span data-ttu-id="c64b6-116">Интерфейс для проверки этой информации — [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span><span class="sxs-lookup"><span data-stu-id="c64b6-116">The interface for examining this information is [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span></span>

<span data-ttu-id="c64b6-117">Сведения о компонентах в документах резервного копирования включают следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="c64b6-117">Component information in Backup Components Documents includes the following:</span></span>

-   <span data-ttu-id="c64b6-118">Только сведения о явно включенных компонентах</span><span class="sxs-lookup"><span data-stu-id="c64b6-118">Only information on explicitly included components</span></span>
-   <span data-ttu-id="c64b6-119">Сведения о метаданных уровня записи, такие как сопоставление альтернативного расположения и восстановление</span><span class="sxs-lookup"><span data-stu-id="c64b6-119">Writer-level metadata information, such as alternate location mappings and restore</span></span>
-   <span data-ttu-id="c64b6-120">Сведения о состоянии, описывающие операцию резервного копирования или восстановления</span><span class="sxs-lookup"><span data-stu-id="c64b6-120">State information describing a backup or restore operation</span></span>

<span data-ttu-id="c64b6-121">В документах компонента резервного копирования не содержатся сведения о [*наборах файлов*](vssgloss-f.md)компонентов.</span><span class="sxs-lookup"><span data-stu-id="c64b6-121">Backup Component Documents do not contain information on components' [*file sets*](vssgloss-f.md).</span></span> <span data-ttu-id="c64b6-122">Документы компонента резервного копирования не предназначены только для чтения и могут быть изменены модулем записи.</span><span class="sxs-lookup"><span data-stu-id="c64b6-122">Backup Component Documents are not read-only and can be modified by the writer.</span></span> <span data-ttu-id="c64b6-123">Интерфейс для доступа к этой информации — [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span><span class="sxs-lookup"><span data-stu-id="c64b6-123">The interface for accessing this information is [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span></span>

<span data-ttu-id="c64b6-124">Жизненный цикл и связь между двумя выражениями компонента можно понять следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c64b6-124">The life cycle and relationship between the two expressions of a component can be understood as follows:</span></span>

-   <span data-ttu-id="c64b6-125">Модули записи отвечают за первоначальные определения компонентов.</span><span class="sxs-lookup"><span data-stu-id="c64b6-125">Writers are responsible for the initial definitions of components.</span></span>
-   <span data-ttu-id="c64b6-126">Инициатор запроса проверяет метаданные всех модулей записи и их компонентов.</span><span class="sxs-lookup"><span data-stu-id="c64b6-126">A requester examines the metadata of all writers and their components.</span></span>
-   <span data-ttu-id="c64b6-127">С помощью выбора компонентов и сведений о логическом пути инициатор запроса определяет, какие компоненты должны быть явно включены, которые могут быть явно включены, определяющие наборы компонентов, а также элементы наборов компонентов.</span><span class="sxs-lookup"><span data-stu-id="c64b6-127">From components' selectability and logical path information, a requester determines which components must be explicitly included, which may be explicitly included, which define component sets, and which are members of component sets.</span></span>
-   <span data-ttu-id="c64b6-128">Инициатор запроса добавляет эти компоненты, требующие явного включения, и неявно включает в себя подкомпоненты в [*наборах компонентов*](/windows) (сведения о которых отсутствуют в документе "компоненты резервного копирования").</span><span class="sxs-lookup"><span data-stu-id="c64b6-128">A requester adds those components that require explicit inclusion, and implicitly includes subcomponents in [*component sets*](/windows) (whose information is not in the Backup Components Document).</span></span>
-   <span data-ttu-id="c64b6-129">При обработке событий модули записи и запрашивающие стороны могут изменять и проверять сведения о компонентах, хранящихся в документе компоненты резервного копирования, чтобы координировать их деятельность.</span><span class="sxs-lookup"><span data-stu-id="c64b6-129">When handling events, writers and requesters may modify and examine the component information stored in the Backup Components Document to coordinate their activity.</span></span>

<span data-ttu-id="c64b6-130">Для правильного выполнения операций резервного копирования и восстановления требуются сведения о компонентах модуля записи и инициатора запроса, и они должны храниться вместе со всеми резервными данными.</span><span class="sxs-lookup"><span data-stu-id="c64b6-130">Both the writer and the requester versions component information are required to properly execute backup and restore operations, and both must be stored with any backed-up data:</span></span>

-   [<span data-ttu-id="c64b6-131">Типы компонентов</span><span class="sxs-lookup"><span data-stu-id="c64b6-131">Component Types</span></span>](component-types.md)
-   [<span data-ttu-id="c64b6-132">Определение компонентов по модулям записи</span><span class="sxs-lookup"><span data-stu-id="c64b6-132">Definition of Components by Writers</span></span>](definition-of-components-by-writers.md)
-   [<span data-ttu-id="c64b6-133">Использование компонентов инициатором запроса</span><span class="sxs-lookup"><span data-stu-id="c64b6-133">Use of Components by the Requester</span></span>](use-of-components-by-the-requestor.md)

 

 
