---
description: Приложения могут использовать PDH для извлечения счетчиков производительности из журналов SQL, а также извлекать форматированные или необработанные счетчики непосредственно из базы данных с помощью запросов SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Схема файла журнала SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663148"
---
# <a name="sql-log-file-schema"></a><span data-ttu-id="4a94a-103">Схема файла журнала SQL</span><span class="sxs-lookup"><span data-stu-id="4a94a-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a94a-104">Поддержка PDH для баз данных SQL ODBC может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="4a94a-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="4a94a-105">Приложения могут использовать интерфейсы API PDH для чтения и записи данных счетчиков производительности в совместимых базах данных SQL ODBC, а затем выполняют дальнейшую обработку с помощью запросов SQL.</span><span class="sxs-lookup"><span data-stu-id="4a94a-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="4a94a-106">В этом разделе описывается схема SQL, используемая для хранения счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="4a94a-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="4a94a-107">Эти сведения можно использовать для создания пользовательских представлений и отчетов.</span><span class="sxs-lookup"><span data-stu-id="4a94a-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="4a94a-108">Схема состоит из следующих трех таблиц:</span><span class="sxs-lookup"><span data-stu-id="4a94a-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="4a94a-109">**каунтердата**</span><span class="sxs-lookup"><span data-stu-id="4a94a-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="4a94a-110">**каунтердетаилс**</span><span class="sxs-lookup"><span data-stu-id="4a94a-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="4a94a-111">**дисплайтоид**</span><span class="sxs-lookup"><span data-stu-id="4a94a-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="4a94a-112">Поддержка PDH для баз данных SQL ODBC работает только с драйверами ODBC SQL, поддерживающими [расширения для операций с массовым копированием (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span><span class="sxs-lookup"><span data-stu-id="4a94a-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
