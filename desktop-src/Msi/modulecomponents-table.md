---
description: Таблица Модулекомпонентс содержит список компонентов, найденных в модуле слияния.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Таблица Модулекомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651072"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="a75eb-103">Таблица Модулекомпонентс</span><span class="sxs-lookup"><span data-stu-id="a75eb-103">ModuleComponents Table</span></span>

<span data-ttu-id="a75eb-104">Таблица Модулекомпонентс содержит список компонентов, найденных в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="a75eb-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="a75eb-105">Таблица Модулекомпонентс содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="a75eb-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="a75eb-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="a75eb-106">Column</span></span>    | <span data-ttu-id="a75eb-107">Type</span><span class="sxs-lookup"><span data-stu-id="a75eb-107">Type</span></span>                         | <span data-ttu-id="a75eb-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="a75eb-108">Key</span></span> | <span data-ttu-id="a75eb-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="a75eb-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="a75eb-110">Компонент</span><span class="sxs-lookup"><span data-stu-id="a75eb-110">Component</span></span> | [<span data-ttu-id="a75eb-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="a75eb-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="a75eb-112">Да</span><span class="sxs-lookup"><span data-stu-id="a75eb-112">Y</span></span>   | <span data-ttu-id="a75eb-113">Нет</span><span class="sxs-lookup"><span data-stu-id="a75eb-113">N</span></span>        |
| <span data-ttu-id="a75eb-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="a75eb-114">ModuleID</span></span>  | [<span data-ttu-id="a75eb-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="a75eb-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="a75eb-116">Да</span><span class="sxs-lookup"><span data-stu-id="a75eb-116">Y</span></span>   | <span data-ttu-id="a75eb-117">Нет</span><span class="sxs-lookup"><span data-stu-id="a75eb-117">N</span></span>        |
| <span data-ttu-id="a75eb-118">Язык</span><span class="sxs-lookup"><span data-stu-id="a75eb-118">Language</span></span>  | [<span data-ttu-id="a75eb-119">Integer</span><span class="sxs-lookup"><span data-stu-id="a75eb-119">Integer</span></span>](integer.md)       | <span data-ttu-id="a75eb-120">Да</span><span class="sxs-lookup"><span data-stu-id="a75eb-120">Y</span></span>   | <span data-ttu-id="a75eb-121">Нет</span><span class="sxs-lookup"><span data-stu-id="a75eb-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a75eb-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="a75eb-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a75eb-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>См</span><span class="sxs-lookup"><span data-stu-id="a75eb-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="a75eb-124">Идентификатор, ссылающийся на компонент в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="a75eb-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="a75eb-125">Столбец Component является внешним ключом к [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a75eb-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="a75eb-126">Запись в столбце Component должна соответствовать соглашению об именовании при [именовании первичных ключей в базах данных модуля слияния](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="a75eb-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="a75eb-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="a75eb-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="a75eb-128">Идентификатор модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a75eb-128">The identifier for the merge module.</span></span> <span data-ttu-id="a75eb-129">Это внешний ключ для [таблицы ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a75eb-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="a75eb-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Языке</span><span class="sxs-lookup"><span data-stu-id="a75eb-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="a75eb-131">Идентификатор языка описывает язык по умолчанию для модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a75eb-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="a75eb-132">Идентификатор языка имеет десятичный формат, например, Английский (США) — 1033.</span><span class="sxs-lookup"><span data-stu-id="a75eb-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="a75eb-133">Внешний ключ к [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a75eb-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a75eb-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a75eb-134">Remarks</span></span>

<span data-ttu-id="a75eb-135">Преобразования языка должны иметь возможность обновлять эту таблицу, если модуль слияния поддерживает несколько языков.</span><span class="sxs-lookup"><span data-stu-id="a75eb-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



