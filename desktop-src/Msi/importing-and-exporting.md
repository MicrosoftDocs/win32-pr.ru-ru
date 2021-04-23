---
description: С помощью установщика можно импортировать текстовый Архив в активную базу данных, а также экспортировать файл базы данных в текстовый Архив. Это может быть полезно для систем управления версиями на основе текста.
ms.assetid: 1025da16-9e1f-4fb4-9ce1-f992970eb903
title: Импортирование и экспортирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb778f4a0fe415686c80f2609f63958ae042d920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155291"
---
# <a name="importing-and-exporting"></a><span data-ttu-id="d54d6-104">Импортирование и экспортирование</span><span class="sxs-lookup"><span data-stu-id="d54d6-104">Importing and Exporting</span></span>

<span data-ttu-id="d54d6-105">С помощью установщика можно импортировать текстовый Архив в активную базу данных, а также экспортировать файл базы данных в текстовый Архив.</span><span class="sxs-lookup"><span data-stu-id="d54d6-105">You can use the installer to import a text archive into an active database as well as to export a database file to a text archive.</span></span> <span data-ttu-id="d54d6-106">Это может быть полезно для систем управления версиями на основе текста.</span><span class="sxs-lookup"><span data-stu-id="d54d6-106">This can be useful for text-based source control systems.</span></span>

<span data-ttu-id="d54d6-107">Чтобы импортировать текстовый Архив в активную базу данных, вызовите функцию [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .</span><span class="sxs-lookup"><span data-stu-id="d54d6-107">To import a text archive into an active database, call the [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) function.</span></span>

<span data-ttu-id="d54d6-108">Чтобы экспортировать файл базы данных в текстовый Архив, вызовите функцию [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) .</span><span class="sxs-lookup"><span data-stu-id="d54d6-108">To export a database file to a text archive, call the [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) function.</span></span>

 

 



