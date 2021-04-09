---
description: Таблица Одбкаттрибуте содержит сведения об атрибутах драйверов и переводчиков ODBC.
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Таблица Одбкаттрибуте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155131"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="bf928-103">Таблица Одбкаттрибуте</span><span class="sxs-lookup"><span data-stu-id="bf928-103">ODBCAttribute Table</span></span>

<span data-ttu-id="bf928-104">Таблица Одбкаттрибуте содержит сведения об атрибутах драйверов и переводчиков ODBC.</span><span class="sxs-lookup"><span data-stu-id="bf928-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="bf928-105">Таблица Одбкаттрибуте содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="bf928-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="bf928-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="bf928-106">Column</span></span>    | <span data-ttu-id="bf928-107">Type</span><span class="sxs-lookup"><span data-stu-id="bf928-107">Type</span></span>                         | <span data-ttu-id="bf928-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="bf928-108">Key</span></span> | <span data-ttu-id="bf928-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="bf928-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="bf928-110">Драйвер\_</span><span class="sxs-lookup"><span data-stu-id="bf928-110">Driver\_</span></span>  | [<span data-ttu-id="bf928-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="bf928-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="bf928-112">Да</span><span class="sxs-lookup"><span data-stu-id="bf928-112">Y</span></span>   | <span data-ttu-id="bf928-113">Нет</span><span class="sxs-lookup"><span data-stu-id="bf928-113">N</span></span>        |
| <span data-ttu-id="bf928-114">attribute</span><span class="sxs-lookup"><span data-stu-id="bf928-114">Attribute</span></span> | [<span data-ttu-id="bf928-115">Text</span><span class="sxs-lookup"><span data-stu-id="bf928-115">Text</span></span>](text.md)             | <span data-ttu-id="bf928-116">Да</span><span class="sxs-lookup"><span data-stu-id="bf928-116">Y</span></span>   | <span data-ttu-id="bf928-117">Нет</span><span class="sxs-lookup"><span data-stu-id="bf928-117">N</span></span>        |
| <span data-ttu-id="bf928-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bf928-118">Value</span></span>     | [<span data-ttu-id="bf928-119">Формате</span><span class="sxs-lookup"><span data-stu-id="bf928-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="bf928-120">Нет</span><span class="sxs-lookup"><span data-stu-id="bf928-120">N</span></span>   | <span data-ttu-id="bf928-121">Да</span><span class="sxs-lookup"><span data-stu-id="bf928-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bf928-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="bf928-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bf928-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Аудиодрайвера\_</span><span class="sxs-lookup"><span data-stu-id="bf928-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="bf928-124">Имя внутреннего маркера для драйвера.</span><span class="sxs-lookup"><span data-stu-id="bf928-124">Internal token name for a driver.</span></span> <span data-ttu-id="bf928-125">Первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf928-125">A primary key for the table.</span></span> <span data-ttu-id="bf928-126">Внешний ключ в [таблице одбкдривер](odbcdriver-table.md).</span><span class="sxs-lookup"><span data-stu-id="bf928-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf928-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию</span><span class="sxs-lookup"><span data-stu-id="bf928-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="bf928-128">Имя атрибута драйвера.</span><span class="sxs-lookup"><span data-stu-id="bf928-128">Name of the driver attribute.</span></span> <span data-ttu-id="bf928-129">Первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf928-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="bf928-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="bf928-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="bf928-131">Локализуемое строковое значение для атрибута.</span><span class="sxs-lookup"><span data-stu-id="bf928-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf928-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf928-132">Remarks</span></span>

<span data-ttu-id="bf928-133">Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="bf928-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="bf928-134">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="bf928-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="bf928-135">Проверка</span><span class="sxs-lookup"><span data-stu-id="bf928-135">Validation</span></span>

<dl>

[<span data-ttu-id="bf928-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="bf928-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bf928-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="bf928-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bf928-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="bf928-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="bf928-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="bf928-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



