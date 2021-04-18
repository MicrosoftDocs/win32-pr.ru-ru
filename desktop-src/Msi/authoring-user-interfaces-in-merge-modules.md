---
description: Для модулей слияния редко требуется пользовательский интерфейс.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Создание пользовательских интерфейсов в модулях слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662931"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="d598e-103">Создание пользовательских интерфейсов в модулях слияния</span><span class="sxs-lookup"><span data-stu-id="d598e-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="d598e-104">Для модулей слияния редко требуется пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d598e-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="d598e-105">Освобождение модуля слияния, который содержит как устанавливаемые компоненты, так и пользовательский интерфейс, в конечном итоге ограничивает гибкость пользователя модуля.</span><span class="sxs-lookup"><span data-stu-id="d598e-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="d598e-106">Объединение компонентов и пользовательского интерфейса в один модуль может помешать разработчикам использовать собственный пользовательский интерфейс или предоставлять автоматическую установку.</span><span class="sxs-lookup"><span data-stu-id="d598e-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="d598e-107">Лучшим вариантом является выпустить два модуля слияния, один из которых автоматически устанавливает компоненты и второй дополнительный модуль, содержащий пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d598e-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="d598e-108">Модуль с пользовательским интерфейсом должен вывести модуль компонента в своей [таблице модуледепенденци](moduledependency-table.md).</span><span class="sxs-lookup"><span data-stu-id="d598e-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="d598e-109">Этот метод позволяет авторам модулей предоставлять пользовательский интерфейс, не вызывая его разработчикам.</span><span class="sxs-lookup"><span data-stu-id="d598e-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="d598e-110">Если таблицы пользовательского интерфейса используются в модулях слияния, их можно объединить так же, как и с любыми другими таблицами.</span><span class="sxs-lookup"><span data-stu-id="d598e-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 



