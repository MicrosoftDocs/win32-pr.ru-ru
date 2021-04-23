---
description: Прежде чем приступить к работе с базой данных, необходимо сначала получить к ней маркер.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Получение маркера базы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155286"
---
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="eaf19-103">Получение маркера базы данных</span><span class="sxs-lookup"><span data-stu-id="eaf19-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="eaf19-104">Прежде чем приступить к работе с базой данных, необходимо сначала получить к ней маркер.</span><span class="sxs-lookup"><span data-stu-id="eaf19-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="eaf19-105">**Доступ к сведениям о базе данных установщика**</span><span class="sxs-lookup"><span data-stu-id="eaf19-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="eaf19-106">Получите маркер базы данных одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="eaf19-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="eaf19-107">Если установка выполняется, получите маркер активной базы данных, вызвав функцию [**метод msigetactivedatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .</span><span class="sxs-lookup"><span data-stu-id="eaf19-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="eaf19-108">Если установка не выполняется, откройте любую из указанных баз данных, вызвав функцию [**мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .</span><span class="sxs-lookup"><span data-stu-id="eaf19-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="eaf19-109">После открытия базы данных можно вызывать функции для получения сведений о базе данных или для работы с базой данных.</span><span class="sxs-lookup"><span data-stu-id="eaf19-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="eaf19-110">Создайте объект **представления** и укажите SQL-запрос к открытой базе данных, вызвав функцию [**мсидатабасеопенвиев**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="eaf19-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="eaf19-111">Получите запись, содержащую все первичные ключи указанной таблицы в открытой базе данных, вызвав функцию [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .</span><span class="sxs-lookup"><span data-stu-id="eaf19-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="eaf19-112">Проверьте текущее состояние открытой базы данных, вызвав функцию [**мсижетдатабасестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) .</span><span class="sxs-lookup"><span data-stu-id="eaf19-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="eaf19-113">С помощью функции **мсижетдатабасестате** можно определить состояние чтения и записи для базы данных или значение, если этот маркер является допустимым.</span><span class="sxs-lookup"><span data-stu-id="eaf19-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



