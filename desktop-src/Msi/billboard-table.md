---
description: В таблице с рекламным объявлением перечислены элементы управления объявлением, отображаемые в полном пользовательском интерфейсе.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Таблица объявлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998264"
---
# <a name="billboard-table"></a><span data-ttu-id="9692e-103">Таблица объявлений</span><span class="sxs-lookup"><span data-stu-id="9692e-103">Billboard Table</span></span>

<span data-ttu-id="9692e-104">В таблице с рекламным объявлением перечислены [элементы управления объявлением](billboard-control.md) , отображаемые в полном пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9692e-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="9692e-105">Таблица объявлений содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="9692e-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="9692e-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="9692e-106">Column</span></span>    | <span data-ttu-id="9692e-107">Type</span><span class="sxs-lookup"><span data-stu-id="9692e-107">Type</span></span>                         | <span data-ttu-id="9692e-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="9692e-108">Key</span></span> | <span data-ttu-id="9692e-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="9692e-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="9692e-110">Печат</span><span class="sxs-lookup"><span data-stu-id="9692e-110">Billboard</span></span> | [<span data-ttu-id="9692e-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9692e-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="9692e-112">Да</span><span class="sxs-lookup"><span data-stu-id="9692e-112">Y</span></span>   | <span data-ttu-id="9692e-113">Нет</span><span class="sxs-lookup"><span data-stu-id="9692e-113">N</span></span>        |
| <span data-ttu-id="9692e-114">Функция\_</span><span class="sxs-lookup"><span data-stu-id="9692e-114">Feature\_</span></span> | [<span data-ttu-id="9692e-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9692e-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="9692e-116">Нет</span><span class="sxs-lookup"><span data-stu-id="9692e-116">N</span></span>   | <span data-ttu-id="9692e-117">Нет</span><span class="sxs-lookup"><span data-stu-id="9692e-117">N</span></span>        |
| <span data-ttu-id="9692e-118">Действие</span><span class="sxs-lookup"><span data-stu-id="9692e-118">Action</span></span>    | [<span data-ttu-id="9692e-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9692e-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="9692e-120">Нет</span><span class="sxs-lookup"><span data-stu-id="9692e-120">N</span></span>   | <span data-ttu-id="9692e-121">Да</span><span class="sxs-lookup"><span data-stu-id="9692e-121">Y</span></span>        |
| <span data-ttu-id="9692e-122">Упорядочение</span><span class="sxs-lookup"><span data-stu-id="9692e-122">Ordering</span></span>  | [<span data-ttu-id="9692e-123">Integer</span><span class="sxs-lookup"><span data-stu-id="9692e-123">Integer</span></span>](integer.md)       | <span data-ttu-id="9692e-124">Нет</span><span class="sxs-lookup"><span data-stu-id="9692e-124">N</span></span>   | <span data-ttu-id="9692e-125">Да</span><span class="sxs-lookup"><span data-stu-id="9692e-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9692e-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="9692e-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9692e-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Печат</span><span class="sxs-lookup"><span data-stu-id="9692e-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="9692e-128">Имя [элемента управления объявлением](billboard-control.md).</span><span class="sxs-lookup"><span data-stu-id="9692e-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="9692e-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="9692e-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="9692e-130">Внешний ключ к первому столбцу [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9692e-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="9692e-131">Объявление отображается только в том случае, если эта функция установлена.</span><span class="sxs-lookup"><span data-stu-id="9692e-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="9692e-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки</span><span class="sxs-lookup"><span data-stu-id="9692e-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="9692e-133">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="9692e-133">The name of an action.</span></span> <span data-ttu-id="9692e-134">Объявление отображается во время выполнения сообщений, полученных от этого действия.</span><span class="sxs-lookup"><span data-stu-id="9692e-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="9692e-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Упорядочение</span><span class="sxs-lookup"><span data-stu-id="9692e-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="9692e-136">При наличии нескольких объявлений, соответствующих действию, они отображаются в порядке, определенном в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="9692e-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="9692e-137">Это число не должно быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="9692e-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="9692e-138">Проверка</span><span class="sxs-lookup"><span data-stu-id="9692e-138">Validation</span></span>

<dl>

[<span data-ttu-id="9692e-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="9692e-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9692e-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="9692e-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9692e-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="9692e-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9692e-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="9692e-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



