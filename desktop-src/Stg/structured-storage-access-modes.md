---
title: Структурированные режимы доступа к хранилищу
description: Для управления одновременным доступом к объекту по нескольким процессам и пользователям необходимы механизмы.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Структурированное хранилище Стрктд STG, основы, функции API, флаги для доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661503"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="d70e6-104">Структурированные режимы доступа к хранилищу</span><span class="sxs-lookup"><span data-stu-id="d70e6-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="d70e6-105">Для управления одновременным доступом к объекту по нескольким процессам и пользователям необходимы механизмы.</span><span class="sxs-lookup"><span data-stu-id="d70e6-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="d70e6-106">COM предоставляет эти механизмы, определяя режимы доступа для объектов хранилища и потоков.</span><span class="sxs-lookup"><span data-stu-id="d70e6-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="d70e6-107">Режим доступа, указанный для родительского объекта хранилища, наследуется его дочерними элементами, хотя можно полагать дополнительные ограничения на дочернее хранилище или поток.</span><span class="sxs-lookup"><span data-stu-id="d70e6-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="d70e6-108">Вложенный объект хранилища или поток может быть открыт в одном и том же режиме или в более ограниченном режиме, чем его родительский элемент, но не может быть открыт в режиме с меньшим уровнем ограничения, чем его родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="d70e6-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="d70e6-109">Режимы доступа задаются с помощью значений, перечисленных в [**константах стгм**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d70e6-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="d70e6-110">Эти значения служат флагами для передачи в качестве аргументов в методы в интерфейсе [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и связанных функциях API.</span><span class="sxs-lookup"><span data-stu-id="d70e6-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="d70e6-111">Как правило, несколько флагов объединяются в параметре *грфмоде* с использованием логической операции **или** .</span><span class="sxs-lookup"><span data-stu-id="d70e6-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="d70e6-112">Флаги делятся на шесть групп.</span><span class="sxs-lookup"><span data-stu-id="d70e6-112">The flags fall into six groups.</span></span> <span data-ttu-id="d70e6-113">В каждый момент времени можно указать только один флаг из каждой группы:</span><span class="sxs-lookup"><span data-stu-id="d70e6-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="d70e6-114">Флаги транзакций</span><span class="sxs-lookup"><span data-stu-id="d70e6-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="d70e6-115">Флаги создания хранилища</span><span class="sxs-lookup"><span data-stu-id="d70e6-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="d70e6-116">Временные флаги создания</span><span class="sxs-lookup"><span data-stu-id="d70e6-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="d70e6-117">Флаги приоритета</span><span class="sxs-lookup"><span data-stu-id="d70e6-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="d70e6-118">Флаги разрешений доступа</span><span class="sxs-lookup"><span data-stu-id="d70e6-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="d70e6-119">Флаги общего доступа</span><span class="sxs-lookup"><span data-stu-id="d70e6-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




