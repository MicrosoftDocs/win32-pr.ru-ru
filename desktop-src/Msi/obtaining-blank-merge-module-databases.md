---
description: Получите пустую базу данных модуля слияния. Вы можете использовать файл Schema. MSM, поставляемый с пакетом SDK для установщик Windows, в качестве начальной базы данных для модуля слияния. Дополнительные сведения см. в разделе Windows SDK Components for установщик Windows Developers.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Получение пустых баз данных модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673531"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="c6b88-105">Получение пустых баз данных модуля слияния</span><span class="sxs-lookup"><span data-stu-id="c6b88-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="c6b88-106">Получите пустую базу данных модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="c6b88-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="c6b88-107">Вы можете использовать файл Schema. MSM, поставляемый с пакетом SDK для установщик Windows, в качестве начальной базы данных для модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="c6b88-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="c6b88-108">Дополнительные сведения см. в разделе [Windows SDK Components for установщик Windows Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c6b88-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="c6b88-109">Разработчики должны создавать модули слияния, используя простейшую схему базы данных, которая устанавливает свои компоненты.</span><span class="sxs-lookup"><span data-stu-id="c6b88-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="c6b88-110">Использование простой схемы гарантирует максимальную совместимость модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="c6b88-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="c6b88-111">Объединение модуля слияния в пакет установки с другой схемой базы данных обычно приводит к конфликтам слияния.</span><span class="sxs-lookup"><span data-stu-id="c6b88-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="c6b88-112">Полный список всех обязательных и необязательных таблиц в модулях слияния см. в разделе [таблицы базы данных модуля слияния](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c6b88-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



