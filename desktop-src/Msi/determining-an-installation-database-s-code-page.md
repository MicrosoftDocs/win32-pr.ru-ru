---
description: Чтобы определить кодовую страницу базы данных, вызовите Мсидатабасикспорт с параметром Хдатабасе, имеющим значение в качестве маркера базы данных, а Сзтабленаме — \_ форцекодепаже.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Определение кодовой страницы базы данных установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910967"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="8a98a-103">Определение кодовой страницы базы данных установки</span><span class="sxs-lookup"><span data-stu-id="8a98a-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="8a98a-104">Чтобы определить кодовую страницу базы данных, вызовите [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) с параметром *хдатабасе* , имеющим значение в качестве маркера базы данных, а *сзтабленаме* — \_ форцекодепаже.</span><span class="sxs-lookup"><span data-stu-id="8a98a-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="8a98a-105">Это экспортирует текстовый файл с расширением IDT.</span><span class="sxs-lookup"><span data-stu-id="8a98a-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="8a98a-106">Первые две строки этого файла пусты.</span><span class="sxs-lookup"><span data-stu-id="8a98a-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="8a98a-107">Третья строка представляет собой номер кодовой страницы ANSI, за которой следует вкладка, за которой следует имя \_ форцекодепаже.</span><span class="sxs-lookup"><span data-stu-id="8a98a-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="8a98a-108">См. также [Обработка кодовых страниц импортированных и экспортированных таблиц](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8a98a-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="8a98a-109">Пример определения кодовой страницы с помощью [**метода Export**](database-export.md) приведен в установщик Windows SDK в составе служебной WiLangId.vbs.</span><span class="sxs-lookup"><span data-stu-id="8a98a-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="8a98a-110">Дополнительные сведения об использовании WiLangId.vbs см. в разделе " [Управление языком и кодовой страницей](manage-language-and-codepage.md)".</span><span class="sxs-lookup"><span data-stu-id="8a98a-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



