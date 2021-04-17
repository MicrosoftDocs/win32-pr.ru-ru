---
description: База данных установщика позволяет разработчику пакета установки управлять переносом приложения из источника в целевой образ.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Использование базы данных установщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673815"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="b8ccf-103">Использование базы данных установщика</span><span class="sxs-lookup"><span data-stu-id="b8ccf-103">Using the Installer Database</span></span>

<span data-ttu-id="b8ccf-104">[База данных установщика](installer-database.md) позволяет разработчику пакета установки управлять переносом приложения из источника в целевой образ.</span><span class="sxs-lookup"><span data-stu-id="b8ccf-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="b8ccf-105">Макет исходного и целевого образов приложения указывается в таблице [Directory](directory-table.md) , а действия, которые устанавливают приложение, указываются в шести таблицах последовательностей:</span><span class="sxs-lookup"><span data-stu-id="b8ccf-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="b8ccf-106">Таблица [инсталлуисекуенце](installuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="b8ccf-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="b8ccf-107">Таблица [инсталлексекутесекуенце](installexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="b8ccf-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="b8ccf-108">Таблица [админуисекуенце](adminuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="b8ccf-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="b8ccf-109">Таблица [админексекутесекуенце](adminexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="b8ccf-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="b8ccf-110">Таблица [адвтуисекуенце](advtuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="b8ccf-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="b8ccf-111">Таблица [адвтексекутесекуенце](advtexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="b8ccf-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="b8ccf-112">В следующих разделах описывается использование [базы данных установщика](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="b8ccf-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="b8ccf-113">Использование таблицы Directory</span><span class="sxs-lookup"><span data-stu-id="b8ccf-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="b8ccf-114">Использование таблицы последовательностей</span><span class="sxs-lookup"><span data-stu-id="b8ccf-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="b8ccf-115">Получение маркера базы данных</span><span class="sxs-lookup"><span data-stu-id="b8ccf-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="b8ccf-116">Фиксация баз данных</span><span class="sxs-lookup"><span data-stu-id="b8ccf-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="b8ccf-117">Импортирование и экспортирование</span><span class="sxs-lookup"><span data-stu-id="b8ccf-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="b8ccf-118">Слияние баз данных</span><span class="sxs-lookup"><span data-stu-id="b8ccf-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="b8ccf-119">Именование настраиваемых таблиц, свойств и действий</span><span class="sxs-lookup"><span data-stu-id="b8ccf-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="b8ccf-120">Ограничения для потоков OLE</span><span class="sxs-lookup"><span data-stu-id="b8ccf-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="b8ccf-121">Работа с запросами</span><span class="sxs-lookup"><span data-stu-id="b8ccf-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="b8ccf-122">Добавление двоичных данных в таблицу с помощью SQL</span><span class="sxs-lookup"><span data-stu-id="b8ccf-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="b8ccf-123">Работа с записями</span><span class="sxs-lookup"><span data-stu-id="b8ccf-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="b8ccf-124">Работа с расположениями папок</span><span class="sxs-lookup"><span data-stu-id="b8ccf-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="b8ccf-125">Указание порядка самостоятельной регистрации</span><span class="sxs-lookup"><span data-stu-id="b8ccf-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="b8ccf-126">Действия по обработке условий, выполняемые во время удаления</span><span class="sxs-lookup"><span data-stu-id="b8ccf-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="b8ccf-127">Вызов функций базы данных из программ</span><span class="sxs-lookup"><span data-stu-id="b8ccf-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="b8ccf-128">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="b8ccf-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="b8ccf-129">Формат определения столбца</span><span class="sxs-lookup"><span data-stu-id="b8ccf-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="b8ccf-130">Определение того, является ли столбец первичным или внешним ключом</span><span class="sxs-lookup"><span data-stu-id="b8ccf-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



