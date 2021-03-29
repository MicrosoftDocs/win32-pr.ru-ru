---
description: Таблицы в группе процедур установки управляют задачами, выполняемыми в ходе установки, с помощью стандартных действий и настраиваемых действий.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Группа таблиц процедур установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349755"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="d6ebc-103">Группа таблиц процедур установки</span><span class="sxs-lookup"><span data-stu-id="d6ebc-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="d6ebc-104">Таблицы в группе процедур установки управляют задачами, выполняемыми в ходе установки, с помощью [стандартных действий](standard-actions.md) и [настраиваемых действий](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d6ebc-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="d6ebc-105">Некоторые из таблиц в этой группе управляют действием высокого уровня, предоставляя последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="d6ebc-106">Каждая из следующих таблиц последовательности управляет частью действия высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="d6ebc-107">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="d6ebc-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="d6ebc-108">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="d6ebc-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="d6ebc-109">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="d6ebc-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="d6ebc-110">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="d6ebc-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="d6ebc-111">Таблица Адвтуисекуенце</span><span class="sxs-lookup"><span data-stu-id="d6ebc-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="d6ebc-112">Таблица Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="d6ebc-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="d6ebc-113">Возможны ситуации, в которых для установки необходимо выполнить действия, которые невозможно использовать только для [стандартных действий](standard-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d6ebc-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="d6ebc-114">Чтобы обеспечить максимальную степень гибкости, установщик предоставляет разработчикам программы установки возможность создавать собственные настраиваемые действия.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="d6ebc-115">Если у вас есть настраиваемые действия, их следует зарегистрировать в установщике, заполнив таблицу CustomAction.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="d6ebc-116">[Таблица CustomAction](customaction-table.md) предоставляет средства для интеграции пользовательского кода и данных в процесс установки.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="d6ebc-117">Код, который выполняется, может быть потоком, содержащимся в базе данных, недавно установленным или существующим исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="d6ebc-118">Следующие таблицы расширяют возможности установщика для работы с файлами и папками во время установки.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="d6ebc-119">[Таблица ремовефиле](removefile-table.md) содержит список файлов, которые удаляются во время установки.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="d6ebc-120">[Таблица ремовеинифиле](removeinifile-table.md) содержит сведения, которые необходимо удалить из ini-файлов приложения.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="d6ebc-121">[Таблица ремоверегистри](removeregistry-table.md) содержит сведения, которые удаляются из системного реестра при выборе соответствующего компонента для установки.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="d6ebc-122">В [таблице креатефолдер](createfolder-table.md) перечислены папки, которые должны быть созданы во время установки.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="d6ebc-123">Хотя установщик создает папки по мере необходимости, они удаляются, как только они будут пустыми.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="d6ebc-124">Список папок в таблице Креатефолдер не удаляется до тех пор, пока компонент не будет удален.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="d6ebc-125">[Таблица MoveFile](movefile-table.md) содержит список файлов, которые будут перемещены или скопированы из указанного исходного каталога на компьютере пользователя в целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="d6ebc-126">Не обязательно использовать таблицу MoveFile для описания файлов, связанных с устанавливаемыми компонентами.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="d6ebc-127">Чтобы настроить необходимые условия, которые должны быть выполнены для запуска установки, заполните таблицу Лаунчкондитион.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="d6ebc-128">[Таблица лаунчкондитион](launchcondition-table.md) содержит список условий, все из которых должны быть удовлетворены для успешного выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 



