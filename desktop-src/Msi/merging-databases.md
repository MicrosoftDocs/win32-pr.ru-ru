---
description: С помощью установщика можно добавить данные в одну базу данных в другую базу данных, выполнив слияние.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Слияние баз данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999105"
---
# <a name="merging-databases"></a><span data-ttu-id="d1622-103">Слияние баз данных</span><span class="sxs-lookup"><span data-stu-id="d1622-103">Merging Databases</span></span>

<span data-ttu-id="d1622-104">С помощью установщика можно добавить данные в одну базу данных в другую базу данных, выполнив слияние.</span><span class="sxs-lookup"><span data-stu-id="d1622-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="d1622-105">Операции [слияния и преобразования](merges-and-transforms.md) выполняются на всей базе данных, а слияние объединяет две базы данных в одну.</span><span class="sxs-lookup"><span data-stu-id="d1622-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="d1622-106">Слияние полезно для групп разработчиков, так как они позволяют разделить базу данных установки крупного приложения на небольшие части и затем объединить их в полную базу данных установки позже.</span><span class="sxs-lookup"><span data-stu-id="d1622-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="d1622-107">**Объединение нескольких баз данных компонентов в одну полную базу данных**</span><span class="sxs-lookup"><span data-stu-id="d1622-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="d1622-108">Разрабатывайте частичные базы данных компонентов отдельно.</span><span class="sxs-lookup"><span data-stu-id="d1622-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="d1622-109">Объедините каждую базу данных компонента в основную базу данных продукта, вызвав функцию [**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .</span><span class="sxs-lookup"><span data-stu-id="d1622-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 



