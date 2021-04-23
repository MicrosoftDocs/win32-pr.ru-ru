---
description: Таблица Component необходима в каждом модуле слияния.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Создание таблиц компонентов модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080683"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="e5b69-103">Создание таблиц компонентов модуля слияния</span><span class="sxs-lookup"><span data-stu-id="e5b69-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="e5b69-104">[Таблица Component](component-table.md) необходима в каждом модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="e5b69-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="e5b69-105">Эта таблица содержит записи для каждого компонента, доставляемого модулем слияния в целевой MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="e5b69-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="e5b69-106">Обратите внимание, что каждый из этих компонентов также должен быть указан в [таблице модулекомпонентс](modulecomponents-table.md) , описанной в разделе [Создание модулекомпонентс таблиц](authoring-modulecomponents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e5b69-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="e5b69-107">Используйте стандартное соглашение об именовании при вводе имен в столбец Component, чтобы гарантировать уникальность идентификатора каждого компонента для всех модулей слияния и баз данных установки.</span><span class="sxs-lookup"><span data-stu-id="e5b69-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="e5b69-108">Дополнительные сведения см. [в разделе именование первичных ключей в базах данных модулей слияния](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="e5b69-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="e5b69-109">Заполните оставшиеся поля в каждой записи, как описано в базе данных установки в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5b69-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="e5b69-110">Компоненты, добавляемые в пакет модулем слияния, должны соответствовать правилам для допустимых установщик Windows компонентов, описанных в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e5b69-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="e5b69-111">Компоненты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="e5b69-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="e5b69-112">Упорядочение приложений по компонентам</span><span class="sxs-lookup"><span data-stu-id="e5b69-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



