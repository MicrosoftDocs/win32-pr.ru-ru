---
description: База данных установщик Windows состоит из множества взаимосвязанных таблиц, которые вместе образуют реляционную базу данных, необходимую для установки группы приложений.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Сведения о базе данных установщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909152"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="0ed47-103">Сведения о базе данных установщика</span><span class="sxs-lookup"><span data-stu-id="0ed47-103">About the Installer Database</span></span>

<span data-ttu-id="0ed47-104">База данных установщик Windows состоит из множества взаимосвязанных таблиц, которые вместе образуют реляционную базу данных, необходимую для установки группы приложений.</span><span class="sxs-lookup"><span data-stu-id="0ed47-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="0ed47-105">Поскольку база данных является реляционной, таблицы связываются по данным в значениях первичного и внешнего ключей.</span><span class="sxs-lookup"><span data-stu-id="0ed47-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="0ed47-106">Это обеспечивает эффективный способ изменения процесса установки и означает, что пользователи могут легко настраивать большое приложение или группу приложений.</span><span class="sxs-lookup"><span data-stu-id="0ed47-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="0ed47-107">Таблицы базы данных соответствуют общему макету всей группы приложений, включая:</span><span class="sxs-lookup"><span data-stu-id="0ed47-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="0ed47-108">Доступные функции</span><span class="sxs-lookup"><span data-stu-id="0ed47-108">Available features</span></span>
-   <span data-ttu-id="0ed47-109">Компоненты</span><span class="sxs-lookup"><span data-stu-id="0ed47-109">Components</span></span>
-   <span data-ttu-id="0ed47-110">Отношение между компонентами и компонентами</span><span class="sxs-lookup"><span data-stu-id="0ed47-110">Relationship between features and components</span></span>
-   <span data-ttu-id="0ed47-111">Необходимые параметры реестра</span><span class="sxs-lookup"><span data-stu-id="0ed47-111">Necessary registry settings</span></span>
-   <span data-ttu-id="0ed47-112">Пользовательский интерфейс для приложения</span><span class="sxs-lookup"><span data-stu-id="0ed47-112">User interface for the application</span></span>

<span data-ttu-id="0ed47-113">Чтобы создать базу данных установки, необходимо заполнить таблицы всеми сведениями о приложениях и процессе установки.</span><span class="sxs-lookup"><span data-stu-id="0ed47-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="0ed47-114">Ручная разработка всех этих таблиц превращается в большую задачу, даже при установке умеренного размера. Поэтому для создания базы данных установщика доступны некоторые сторонние средства.</span><span class="sxs-lookup"><span data-stu-id="0ed47-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="0ed47-115">В следующих разделах описываются группы связанных таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="0ed47-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="0ed47-116">Группа основных таблиц</span><span class="sxs-lookup"><span data-stu-id="0ed47-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="0ed47-117">Группа таблиц файлов</span><span class="sxs-lookup"><span data-stu-id="0ed47-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="0ed47-118">Группа таблиц реестра</span><span class="sxs-lookup"><span data-stu-id="0ed47-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="0ed47-119">Группа системных таблиц</span><span class="sxs-lookup"><span data-stu-id="0ed47-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="0ed47-120">Группа "таблицы указателей"</span><span class="sxs-lookup"><span data-stu-id="0ed47-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="0ed47-121">Группа "таблицы сведений о программах"</span><span class="sxs-lookup"><span data-stu-id="0ed47-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="0ed47-122">Группа таблиц процедур установки</span><span class="sxs-lookup"><span data-stu-id="0ed47-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="0ed47-123">Условные обозначения диаграммы отношений сущностей</span><span class="sxs-lookup"><span data-stu-id="0ed47-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="0ed47-124">Файлы архивов текста</span><span class="sxs-lookup"><span data-stu-id="0ed47-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="0ed47-125">Полный список всех таблиц в базе данных установки см. в разделе [таблицы базы данных](database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0ed47-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ed47-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0ed47-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed47-127">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="0ed47-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



