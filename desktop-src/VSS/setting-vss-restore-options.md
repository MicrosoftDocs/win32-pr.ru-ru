---
description: Параметры восстановления позволяют запрашивающим устройствам передавать настраиваемые параметры восстановления в модули записи.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Настройка параметров восстановления VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692875"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="da690-103">Настройка параметров восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="da690-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="da690-104">Параметры восстановления позволяют запрашивающим устройствам передавать настраиваемые параметры восстановления в модули записи.</span><span class="sxs-lookup"><span data-stu-id="da690-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="da690-105">Параметры восстановления</span><span class="sxs-lookup"><span data-stu-id="da690-105">Restore Options</span></span>

<span data-ttu-id="da690-106">Стандартизация формата параметров восстановления позволяет модулям записи и инициаторам обработки распространенных пользовательских запросов.</span><span class="sxs-lookup"><span data-stu-id="da690-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="da690-107">Параметры восстановления задаются инициатором запроса путем вызова метода [**ивссбаккупкомпонентс:: сетрестореоптионс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) до одного раза на выбранный компонент для резервного копирования перед вызовом метода [**rerestore ивссбаккупкомпонентс::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .</span><span class="sxs-lookup"><span data-stu-id="da690-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="da690-108">Строка, передаваемая в параметр *всзрестореоптионс* методу **сетрестореоптионс** , может содержать несколько значений, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="da690-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="da690-109">Формат</span><span class="sxs-lookup"><span data-stu-id="da690-109">Format</span></span>

<span data-ttu-id="da690-110">Формат параметров восстановления представляет собой одну или несколько пар "имя-значение", разделенных запятыми, и имя, по желанию, имя подкомпонента, к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="da690-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="da690-111">Имена компонентов и имена параметров не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="da690-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="da690-112">Чувствительность к регистру значений определяется модулем записи.</span><span class="sxs-lookup"><span data-stu-id="da690-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="da690-113">Пример:</span><span class="sxs-lookup"><span data-stu-id="da690-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="da690-114">В этом примере "параметр1" применяется только к подкомпоненту "child1" и его потомкам, параметр "параметр2" применяется ко всем компонентам и их потомкам, а "Option3" применяется только к \\ подкомпонентам "Child2 Grandchild3" и его потомкам.</span><span class="sxs-lookup"><span data-stu-id="da690-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="da690-115">Метод [**сетрестореоптионс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) может быть вызван только для компонентов, которые могут быть выбраны для резервного копирования, тогда как узлы-потомки нельзя выбирать для резервного копирования, они могут быть доступны для восстановления.</span><span class="sxs-lookup"><span data-stu-id="da690-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="da690-116">Общие параметры восстановления</span><span class="sxs-lookup"><span data-stu-id="da690-116">Common Restore Options</span></span>

<span data-ttu-id="da690-117">Эти общие параметры восстановления были определены для повышения совместимости между модулями записи и запрашивающими стороны.</span><span class="sxs-lookup"><span data-stu-id="da690-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="da690-118">Заслуживающего</span><span class="sxs-lookup"><span data-stu-id="da690-118">Authoritative</span></span>

    <span data-ttu-id="da690-119">Параметр "полномочное" поддерживает несколько значений "элемент", но только одно значение "все".</span><span class="sxs-lookup"><span data-stu-id="da690-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="da690-120">Весь этот компонент является полномочным.</span><span class="sxs-lookup"><span data-stu-id="da690-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="da690-121">Только указанный элемент является полномочным.</span><span class="sxs-lookup"><span data-stu-id="da690-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="da690-122">Формат именованного элемента определяется модулем записи.</span><span class="sxs-lookup"><span data-stu-id="da690-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="da690-123">Распространенными конструкциями являются " \* " для обозначения всех файлов, "..." для указания всех файлов и подкаталогов указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="da690-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="da690-124">Накат</span><span class="sxs-lookup"><span data-stu-id="da690-124">Roll Forward</span></span>

    <span data-ttu-id="da690-125">После восстановления базы данных модули записи обычно направляются в журналы, чтобы обеспечить актуальность базы данных.</span><span class="sxs-lookup"><span data-stu-id="da690-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="da690-126">В случае добавочного или разностного восстановления инициатор запроса использует метод [**ивссбаккупкомпонентс:: сетаддитионалресторес**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) для частичного управления поведением обработки журнала. Этот вариант восстановления позволяет более детально управлять.</span><span class="sxs-lookup"><span data-stu-id="da690-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="da690-127">Не переносите журналы.</span><span class="sxs-lookup"><span data-stu-id="da690-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="da690-128">Выполните все журналы.</span><span class="sxs-lookup"><span data-stu-id="da690-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="da690-129">Накат журналов до указанной точки.</span><span class="sxs-lookup"><span data-stu-id="da690-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="da690-130">Формат указанной точки определяется модулем записи.</span><span class="sxs-lookup"><span data-stu-id="da690-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="da690-131">Имя нового компонента</span><span class="sxs-lookup"><span data-stu-id="da690-131">New Component Name</span></span>

    <span data-ttu-id="da690-132">Модуль записи может потребоваться восстановить новое имя компонента.</span><span class="sxs-lookup"><span data-stu-id="da690-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="da690-133">Например, восстановление базы данных с другим именем для восстановления отдельного элемента; При восстановлении с тем же именем все данные мы рекомендуем, чтобы модули записи приняли допустимый логический путь и имя компонента в качестве значения этого параметра.</span><span class="sxs-lookup"><span data-stu-id="da690-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="da690-134">Это часто будет использоваться с [*направленным целевым объектом*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="da690-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



