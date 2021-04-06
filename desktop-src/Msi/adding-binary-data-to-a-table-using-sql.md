---
description: Двоичные данные не могут быть вставлены в таблицу непосредственно с помощью инструкций INSERT INTO или UPDATE SQL.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Добавление двоичных данных в таблицу с помощью SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491bfe57354b4faf9f7c385bc4e14c64ad366f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909143"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a><span data-ttu-id="f63ef-103">Добавление двоичных данных в таблицу с помощью SQL</span><span class="sxs-lookup"><span data-stu-id="f63ef-103">Adding Binary Data to a Table Using SQL</span></span>

<span data-ttu-id="f63ef-104">Двоичные данные не могут быть вставлены в таблицу непосредственно с помощью инструкций INSERT INTO или UPDATE SQL.</span><span class="sxs-lookup"><span data-stu-id="f63ef-104">Binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="f63ef-105">Чтобы добавить двоичные данные в таблицу, необходимо сначала использовать маркер параметра (?) в запросе в качестве заполнителя для двоичного значения.</span><span class="sxs-lookup"><span data-stu-id="f63ef-105">In order to add binary data to a table, you must first use the parameter marker (?) in the query as a placeholder for the binary value.</span></span> <span data-ttu-id="f63ef-106">Выполнение запроса должно включать запись, содержащую двоичные данные в одном из полей.</span><span class="sxs-lookup"><span data-stu-id="f63ef-106">The execution of the query should include a record that contains the binary data in one of its fields.</span></span>

<span data-ttu-id="f63ef-107">Маркер — это ссылка на параметр для значения, предоставленного в записи, отправленной с помощью запроса.</span><span class="sxs-lookup"><span data-stu-id="f63ef-107">A marker is a parameter reference to a value supplied by a record submitted with the query.</span></span> <span data-ttu-id="f63ef-108">Он представлен в инструкции SQL вопросительным знаком (?).</span><span class="sxs-lookup"><span data-stu-id="f63ef-108">It is represented in the SQL statement by a question mark (?).</span></span>

<span data-ttu-id="f63ef-109">В следующем примере кода в таблицу добавляются двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="f63ef-109">The following sample code adds binary data to a table.</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")


int main()  
{ 

PMSIHANDLE hDatabase = 0;
PMSIHANDLE hView = 0;
PMSIHANDLE hRec = 0;

if (ERROR_SUCCESS == MsiOpenDatabase(_T("c:\\temp\\testdb.msi"), MSIDBOPEN_TRANSACT, &hDatabase))
{
    //
    // Open view on Binary table so that we can add a new row, must use '?' to represent Binary data
    //

    if (ERROR_SUCCESS == MsiDatabaseOpenView(hDatabase, _T("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)"), &hView))
    {

        //
        // Create record with binary data in 1st field (must match up with '?' in query)
        //

        hRec = MsiCreateRecord(1);
        if (ERROR_SUCCESS == MsiRecordSetStream(hRec, 1, _T("c:\\temp\\data.bin")))
        {

            //
            // Execute view with record containing binary data value; commit database to save changes
            //

            if (ERROR_SUCCESS == MsiViewExecute(hView, hRec)
              && ERROR_SUCCESS == MsiViewClose(hView)
              && ERROR_SUCCESS == MsiDatabaseCommit(hDatabase))
            {
                //
                // New binary data successfully committed to the database
                //
            }
        }
    }
}

return 0;  
}
```



<span data-ttu-id="f63ef-110">Следующий пример скрипта добавляет в таблицу двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="f63ef-110">The following sample script adds binary data to a table.</span></span>


```VB
Dim Installer
Dim Database
Dim View
Dim Record

Set Installer = CreateObject("WindowsInstaller.Installer")

Set Record = Installer.CreateRecord(1)
Record.SetStream 1, "c:\temp\data.bin"

Set Database = Installer.OpenDatabase("c:\temp\testdb.msi", msiOpenDatabaseModeTransact)
Set View = Database.OpenView("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)")
View.Execute Record
Database.Commit ' save changes
```



## <a name="related-topics"></a><span data-ttu-id="f63ef-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f63ef-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f63ef-112">Работа с запросами</span><span class="sxs-lookup"><span data-stu-id="f63ef-112">Working with Queries</span></span>](working-with-queries.md)
</dt> <dt>

[<span data-ttu-id="f63ef-113">Синтаксис SQL</span><span class="sxs-lookup"><span data-stu-id="f63ef-113">SQL Syntax</span></span>](sql-syntax.md)
</dt> <dt>

[<span data-ttu-id="f63ef-114">Примеры запросов к базе данных с помощью SQL и скрипта</span><span class="sxs-lookup"><span data-stu-id="f63ef-114">Examples of Database Queries Using SQL and Script</span></span>](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



