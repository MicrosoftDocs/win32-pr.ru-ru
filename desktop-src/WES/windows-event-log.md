---
title: Журнал событий Windows
description: API журнала событий Windows определяет схему, используемую для записи манифеста инструментирования.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891057"
---
# <a name="windows-event-log"></a><span data-ttu-id="540c8-103">Журнал событий Windows</span><span class="sxs-lookup"><span data-stu-id="540c8-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="540c8-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="540c8-104">Purpose</span></span>

<span data-ttu-id="540c8-105">API журнала событий Windows определяет схему, используемую для записи манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="540c8-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="540c8-106">Манифест инструментирования определяет поставщика событий и события, которые он регистрирует.</span><span class="sxs-lookup"><span data-stu-id="540c8-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="540c8-107">API также включает функции, которые потребитель событий, например [Просмотр событий](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), будет использовать для чтения и отрисовки событий.</span><span class="sxs-lookup"><span data-stu-id="540c8-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="540c8-108">Для записи событий, определенных в манифесте, используйте функции, входящие в API [трассировки событий](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="540c8-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="540c8-109">Журнал событий Windows заменяет API [регистрации событий](/windows/desktop/EventLog/event-logging) , начиная с операционной системы Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="540c8-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="540c8-110">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="540c8-110">Developer audience</span></span>

<span data-ttu-id="540c8-111">Журнал событий Windows предназначен для программистов C/C++.</span><span class="sxs-lookup"><span data-stu-id="540c8-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="540c8-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="540c8-112">Run-time requirements</span></span>

<span data-ttu-id="540c8-113">Журнал событий Windows включен в операционную систему, начиная с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="540c8-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="540c8-114">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="540c8-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="540c8-115">Полный журнал версий см. в разделе [новые](what-s-new.md)возможности.</span><span class="sxs-lookup"><span data-stu-id="540c8-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="540c8-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="540c8-116">In this section</span></span>


| <span data-ttu-id="540c8-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="540c8-117">Topic</span></span>                                                        | <span data-ttu-id="540c8-118">Описание</span><span class="sxs-lookup"><span data-stu-id="540c8-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="540c8-119">Использование журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="540c8-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="540c8-120">Процедурное руководство, в котором показано, как использовать API журнала событий Windows.</span><span class="sxs-lookup"><span data-stu-id="540c8-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="540c8-121">Справочник по журналам событий Windows</span><span class="sxs-lookup"><span data-stu-id="540c8-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="540c8-122">Типы данных, функции, перечисления, структуры, константы и схемы, которые включает API.</span><span class="sxs-lookup"><span data-stu-id="540c8-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|