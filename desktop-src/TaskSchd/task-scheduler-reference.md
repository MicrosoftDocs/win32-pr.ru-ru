---
title: Справочник по планировщик задач
description: В этом разделе описываются API-интерфейсы, объекты скриптов и схема XML, предоставляемая планировщик задач.
ms.assetid: e3b5a1e1-4d18-44b7-aaa6-ebec11892bec
keywords:
- Планировщик задач планировщик задач, справочные материалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb22306266054b8ec19a90f188c43e5eb7e4393b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776094"
---
# <a name="task-scheduler-reference"></a><span data-ttu-id="0cfca-104">Справочник по планировщик задач</span><span class="sxs-lookup"><span data-stu-id="0cfca-104">Task Scheduler Reference</span></span>

<span data-ttu-id="0cfca-105">В этом разделе описываются API-интерфейсы, объекты скриптов и схема XML, предоставляемая планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0cfca-105">This section describes the APIs, scripting objects, and XML schema that are provided by the Task Scheduler.</span></span>

<span data-ttu-id="0cfca-106">Темы API включают описание API, синтаксис объявления API, примечания, описывающие особые условия для API, и блок требований, который описывает, какие платформы, файлы заголовков и библиотеки требуются.</span><span class="sxs-lookup"><span data-stu-id="0cfca-106">API topics include a description of the API, the declaration syntax of the API, remarks that describe special conditions for the API, and a requirements block that describes what platform, header files, and libraries are required.</span></span>

<span data-ttu-id="0cfca-107">Разделы, посвященные объектам сценариев, включают описание объекта, синтаксис объявления объекта, примечания, описывающие особые условия для объекта, и блок требований, который описывает, какие платформы и библиотеки типов требуются.</span><span class="sxs-lookup"><span data-stu-id="0cfca-107">Scripting object topics include a description of the object, the declaration syntax of the object, remarks that describe special conditions for the object, and a requirements block that describes what platform and type libraries are required.</span></span>

<span data-ttu-id="0cfca-108">Темы схемы XML включают описание элемента, сведения о родительском, дочернем элементе и атрибутах, а также примечания, описывающие особые условия.</span><span class="sxs-lookup"><span data-stu-id="0cfca-108">XML schema topics include a description of the element, parent, child, and attribute information, and remarks that describe special conditions.</span></span>



| <span data-ttu-id="0cfca-109">См.</span><span class="sxs-lookup"><span data-stu-id="0cfca-109">See</span></span>                                                                                          | <span data-ttu-id="0cfca-110">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="0cfca-110">For information on</span></span>                                                                                                                            |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cfca-111">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="0cfca-111">Task Scheduler Objects</span></span>](task-scheduler-objects.md)                                         | <span data-ttu-id="0cfca-112">Создание скриптов для объектов и их методов и свойств.</span><span class="sxs-lookup"><span data-stu-id="0cfca-112">Scripting objects and their methods and properties.</span></span>                                                                                           |
| [<span data-ttu-id="0cfca-113">Интерфейсы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="0cfca-113">Task Scheduler Interfaces</span></span>](task-scheduler-interfaces.md)                                   | <span data-ttu-id="0cfca-114">Интерфейсы и их методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="0cfca-114">Interfaces and their methods and properties.</span></span>                                                                                                  |
| [<span data-ttu-id="0cfca-115">планировщик задач структур и объединений</span><span class="sxs-lookup"><span data-stu-id="0cfca-115">Task Scheduler Structures and Unions</span></span>](task-scheduler-structures-and-unions.md)             | <span data-ttu-id="0cfca-116">Структуры и объединения.</span><span class="sxs-lookup"><span data-stu-id="0cfca-116">Structures and unions.</span></span>                                                                                                                        |
| [<span data-ttu-id="0cfca-117">планировщик задач перечислимых типов</span><span class="sxs-lookup"><span data-stu-id="0cfca-117">Task Scheduler Enumerated Types</span></span>](task-scheduler-enumerated-types.md)                       | <span data-ttu-id="0cfca-118">Константы, определяемые перечислителями.</span><span class="sxs-lookup"><span data-stu-id="0cfca-118">Constants defined by enumerators.</span></span>                                                                                                             |
| [<span data-ttu-id="0cfca-119">Схема планировщик задач</span><span class="sxs-lookup"><span data-stu-id="0cfca-119">Task Scheduler Schema</span></span>](task-scheduler-schema.md)                                           | <span data-ttu-id="0cfca-120">Элементы, простые типы, сложные типы и группы атрибутов, определяемые схемой.</span><span class="sxs-lookup"><span data-stu-id="0cfca-120">Elements, simple types, complex types, and attribute groups defined by the schema.</span></span>                                                            |
| [<span data-ttu-id="0cfca-121">планировщик задач константы ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0cfca-121">Task Scheduler Error and Success Constants</span></span>](task-scheduler-error-and-success-constants.md) | <span data-ttu-id="0cfca-122">Константы Error и Success, возвращаемые API-интерфейсами планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0cfca-122">Error and success constants returned by Task Scheduler APIs.</span></span>                                                                                  |
| [<span data-ttu-id="0cfca-123">**Schtasks.exe**</span><span class="sxs-lookup"><span data-stu-id="0cfca-123">**Schtasks.exe**</span></span>](schtasks.md)                                                             | <span data-ttu-id="0cfca-124">Средство командной строки Schtasks.exe, которое используется для создания, удаления, запроса, изменения, запуска и завершения запланированных задач на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0cfca-124">The Schtasks.exe command line tool that is used to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0cfca-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0cfca-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cfca-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0cfca-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




