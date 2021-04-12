---
description: Таблицы в группе системных таблиц следят за таблицами и столбцами базы данных установки.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Группа системных таблиц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155115"
---
# <a name="system-tables-group"></a><span data-ttu-id="33f6a-103">Группа системных таблиц</span><span class="sxs-lookup"><span data-stu-id="33f6a-103">System Tables Group</span></span>

<span data-ttu-id="33f6a-104">Таблицы в группе системных таблиц следят за таблицами и столбцами базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="33f6a-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="33f6a-105">[ \_ Таблица](-tables-table.md) Tables отслеживает все таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="33f6a-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="33f6a-106">Сюда входят таблицы, которые могли быть созданы для собственных настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="33f6a-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="33f6a-107">Запросите эту таблицу, чтобы узнать, существует ли таблица.</span><span class="sxs-lookup"><span data-stu-id="33f6a-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="33f6a-108">[ \_ Таблица Columns](-columns-table.md) отслеживает столбцы в базе данных установки.</span><span class="sxs-lookup"><span data-stu-id="33f6a-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="33f6a-109">Временные столбцы в настоящее время не записываются этой таблицей.</span><span class="sxs-lookup"><span data-stu-id="33f6a-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="33f6a-110">Запросите эту таблицу, чтобы узнать, существует ли данный столбец.</span><span class="sxs-lookup"><span data-stu-id="33f6a-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="33f6a-111">В [ \_ таблице Streams](-streams-table.md) перечислены внедренные потоки данных OLE.</span><span class="sxs-lookup"><span data-stu-id="33f6a-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="33f6a-112">В [ \_ таблице хранения](-storages-table.md) перечислены внедренные хранилища данных OLE.</span><span class="sxs-lookup"><span data-stu-id="33f6a-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="33f6a-113">[ \_ Таблица проверки](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="33f6a-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="33f6a-114">\_Таблица проверки отслеживает типы и допустимые диапазоны каждого столбца в базе данных.</span><span class="sxs-lookup"><span data-stu-id="33f6a-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="33f6a-115">\_Таблица проверки используется в процессе проверки базы данных, чтобы убедиться в том, что все столбцы включены в учет и имеют правильные значения.</span><span class="sxs-lookup"><span data-stu-id="33f6a-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="33f6a-116">Эта таблица не поставляется с базой данных установщика.</span><span class="sxs-lookup"><span data-stu-id="33f6a-116">This table is not shipped with the installer database.</span></span>

 

 



