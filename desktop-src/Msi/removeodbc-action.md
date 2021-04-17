---
description: Действие Ремовеодбк удаляет источники данных, переводчики и драйверы, перечисленные для удаления во время установки.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Действие Ремовеодбк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663375"
---
# <a name="removeodbc-action"></a><span data-ttu-id="a778d-103">Действие Ремовеодбк</span><span class="sxs-lookup"><span data-stu-id="a778d-103">RemoveODBC Action</span></span>

<span data-ttu-id="a778d-104">Действие Ремовеодбк удаляет источники данных, переводчики и драйверы, перечисленные для удаления во время установки.</span><span class="sxs-lookup"><span data-stu-id="a778d-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="a778d-105">Это действие запрашивает таблицу [одбкдатасаурце](odbcdatasource-table.md), [таблицу Одбктранслатор](odbctranslator-table.md)и [таблицу одбкдривер](odbcdriver-table.md) для каждого источника данных, переводчика или драйвера, запланированного для удаления.</span><span class="sxs-lookup"><span data-stu-id="a778d-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a778d-106">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="a778d-106">Sequence Restrictions</span></span>

<span data-ttu-id="a778d-107">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="a778d-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a778d-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="a778d-108">ActionData Messages</span></span>

<span data-ttu-id="a778d-109">Для каждого установленного драйвера.</span><span class="sxs-lookup"><span data-stu-id="a778d-109">For each driver installed.</span></span>



| <span data-ttu-id="a778d-110">Поле</span><span class="sxs-lookup"><span data-stu-id="a778d-110">Field</span></span> | <span data-ttu-id="a778d-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="a778d-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="a778d-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a778d-112">\[1\]</span></span> | <span data-ttu-id="a778d-113">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="a778d-113">Driver description.</span></span> <span data-ttu-id="a778d-114">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a778d-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="a778d-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a778d-115">\[2\]</span></span> | <span data-ttu-id="a778d-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="a778d-116">ComponentId</span></span>                              |



 

<span data-ttu-id="a778d-117">Для каждого установленного транслятора.</span><span class="sxs-lookup"><span data-stu-id="a778d-117">For each translator installed.</span></span>



| <span data-ttu-id="a778d-118">Поле</span><span class="sxs-lookup"><span data-stu-id="a778d-118">Field</span></span> | <span data-ttu-id="a778d-119">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="a778d-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="a778d-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a778d-120">\[1\]</span></span> | <span data-ttu-id="a778d-121">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="a778d-121">Driver description.</span></span> <span data-ttu-id="a778d-122">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a778d-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="a778d-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a778d-123">\[2\]</span></span> | <span data-ttu-id="a778d-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="a778d-124">ComponentId</span></span>                              |



 

<span data-ttu-id="a778d-125">Для каждого установленного источника данных.</span><span class="sxs-lookup"><span data-stu-id="a778d-125">For each data source installed.</span></span>



| <span data-ttu-id="a778d-126">Поле</span><span class="sxs-lookup"><span data-stu-id="a778d-126">Field</span></span> | <span data-ttu-id="a778d-127">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="a778d-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="a778d-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a778d-128">\[1\]</span></span> | <span data-ttu-id="a778d-129">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="a778d-129">Driver description.</span></span> <span data-ttu-id="a778d-130">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a778d-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="a778d-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a778d-131">\[2\]</span></span> | <span data-ttu-id="a778d-132">ComponentId</span><span class="sxs-lookup"><span data-stu-id="a778d-132">ComponentId</span></span>                                             |
| <span data-ttu-id="a778d-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a778d-133">\[3\]</span></span> | <span data-ttu-id="a778d-134">Регистрация: SQL \_ Remove \_ DSN или SQL \_ Remove \_ sys \_ DSN</span><span class="sxs-lookup"><span data-stu-id="a778d-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a778d-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a778d-135">Remarks</span></span>

<span data-ttu-id="a778d-136">Если счетчик использования ODBC и счетчик использования файлов становятся нулями, файл удаляется.</span><span class="sxs-lookup"><span data-stu-id="a778d-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="a778d-137">Регистрация зависит от количества использований ODBC, и удаление файлов основано на счетчиках общего числа ссылок на библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a778d-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



