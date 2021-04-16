---
description: В каждом модуле слияния требуется пустая таблица Феатурекомпонентс. Эта пустая таблица содержит схему для средства слияния, если в целевом MSI-файле отсутствует собственная таблица Феатурекомпонентс.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Создание таблиц Феатурекомпонентс для модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662941"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a><span data-ttu-id="844bc-104">Создание таблиц Феатурекомпонентс для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="844bc-104">Authoring Merge Module FeatureComponents Tables</span></span>

<span data-ttu-id="844bc-105">В каждом модуле слияния требуется пустая [Таблица феатурекомпонентс](featurecomponents-table.md) .</span><span class="sxs-lookup"><span data-stu-id="844bc-105">A blank [FeatureComponents table](featurecomponents-table.md) is required in every merge module.</span></span> <span data-ttu-id="844bc-106">Эта пустая таблица содержит схему для средства слияния, если в целевом MSI-файле отсутствует собственная таблица Феатурекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="844bc-106">This empty table provides a schema for the merge tool if the target .msi file does not have its own FeatureComponents table.</span></span>

<span data-ttu-id="844bc-107">Если, и только если, в целевом MSI-файле отсутствует таблица Феатурекомпонентс, то средство слияния использует пустую таблицу, указанную в модуле.</span><span class="sxs-lookup"><span data-stu-id="844bc-107">If, and only if, there is no FeatureComponents table in the target .msi file does the merge tool use the blank table provided in the module.</span></span> <span data-ttu-id="844bc-108">В этом случае средство слияния создает повторяющуюся таблицу в файле Target. msi и добавляет строки, связывающие новые компоненты в модуле слияния с компонентами пакета установки приложения.</span><span class="sxs-lookup"><span data-stu-id="844bc-108">In this case, the merge tool creates a duplicate table in the target .msi file and adds rows that associate the new components in the merge module to the features in the application's installation package.</span></span>

 

 



