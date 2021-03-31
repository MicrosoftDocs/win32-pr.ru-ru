---
description: Изменения, вносимые в базу данных установки, не записываются в базу данных до тех пор, пока не будет вызван Мсидатабасекоммит.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Фиксация баз данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911343"
---
# <a name="committing-databases"></a><span data-ttu-id="bc3fd-103">Фиксация баз данных</span><span class="sxs-lookup"><span data-stu-id="bc3fd-103">Committing Databases</span></span>

<span data-ttu-id="bc3fd-104">Изменения, вносимые в базу данных установки, не записываются в базу данных до тех пор, пока не будет вызван [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="bc3fd-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="bc3fd-105">**Проверка завершения изменений, внесенных в базу данных**</span><span class="sxs-lookup"><span data-stu-id="bc3fd-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="bc3fd-106">Проверьте, будет ли записана таблица при вызове [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) путем вызова [**мсидатабасеистаблеперсистент**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span><span class="sxs-lookup"><span data-stu-id="bc3fd-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="bc3fd-107">Вызовите функцию [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) , чтобы завершить изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="bc3fd-108">Изменения, внесенные в базу данных, накапливаются и не отражаются в реальной базе данных до тех пор, пока не будет вызван [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="bc3fd-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="bc3fd-109">Временные столбцы или строки не фиксируются в базе данных.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="bc3fd-110">При закрытии базы данных все изменения, внесенные с момента последнего **мсидатабасекоммит** , автоматически откатываются.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



