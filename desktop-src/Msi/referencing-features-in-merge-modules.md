---
description: Модули слияния работают только с компонентами, а не с функциями. Однако некоторые таблицы в модулях слияния, например в таблице Публишкомпонент, содержат поля, которые ссылаются на функции.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Создание ссылок на функции в модулях слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998418"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="80227-104">Создание ссылок на функции в модулях слияния</span><span class="sxs-lookup"><span data-stu-id="80227-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="80227-105">Модули слияния работают только с компонентами, а не с функциями.</span><span class="sxs-lookup"><span data-stu-id="80227-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="80227-106">Однако некоторые таблицы в модулях слияния, например в [таблице публишкомпонент](publishcomponent-table.md), содержат поля, которые ссылаются на функции.</span><span class="sxs-lookup"><span data-stu-id="80227-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="80227-107">Пустой GUID: {00000000-0000-0000-0000-000000000000} должен быть создан в любом поле базы данных модуля слияния, которое ссылается на функцию.</span><span class="sxs-lookup"><span data-stu-id="80227-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="80227-108">При слиянии модуля слияния с пакетом установки средство слияния заменяет нулевое значение GUID на функцию, указанную в пакете установки, за исключением таблиц, требующих специальной обработки, таких как [Таблица ModuleSignature](modulesignature-table.md) и таблицы модулесекуенце.</span><span class="sxs-lookup"><span data-stu-id="80227-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="80227-109">Обратите внимание, что если в качестве первичного ключа используется идентификатор GUID null, то не гарантируется, что значение, заданное средством слияния, является уникальным.</span><span class="sxs-lookup"><span data-stu-id="80227-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="80227-110">Авторы модулей слияния отвечают за то, что существующий первичный ключ в пользовательском интерфейсе не повторяется, когда средство слияния заменяет пустые GUID с помощью функций.</span><span class="sxs-lookup"><span data-stu-id="80227-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



