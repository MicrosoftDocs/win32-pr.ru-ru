---
description: Таблица Одбксаурцеаттрибуте содержит сведения об атрибутах источников данных.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Таблица Одбксаурцеаттрибуте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541055"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="d548b-103">Таблица Одбксаурцеаттрибуте</span><span class="sxs-lookup"><span data-stu-id="d548b-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="d548b-104">Таблица Одбксаурцеаттрибуте содержит сведения об атрибутах источников данных.</span><span class="sxs-lookup"><span data-stu-id="d548b-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="d548b-105">Таблица Одбксаурцеаттрибуте содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="d548b-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="d548b-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="d548b-106">Column</span></span>       | <span data-ttu-id="d548b-107">Type</span><span class="sxs-lookup"><span data-stu-id="d548b-107">Type</span></span>                         | <span data-ttu-id="d548b-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="d548b-108">Key</span></span> | <span data-ttu-id="d548b-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d548b-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="d548b-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="d548b-110">DataSource\_</span></span> | [<span data-ttu-id="d548b-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d548b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d548b-112">Да</span><span class="sxs-lookup"><span data-stu-id="d548b-112">Y</span></span>   | <span data-ttu-id="d548b-113">Нет</span><span class="sxs-lookup"><span data-stu-id="d548b-113">N</span></span>        |
| <span data-ttu-id="d548b-114">attribute</span><span class="sxs-lookup"><span data-stu-id="d548b-114">Attribute</span></span>    | [<span data-ttu-id="d548b-115">Text</span><span class="sxs-lookup"><span data-stu-id="d548b-115">Text</span></span>](text.md)             | <span data-ttu-id="d548b-116">Да</span><span class="sxs-lookup"><span data-stu-id="d548b-116">Y</span></span>   | <span data-ttu-id="d548b-117">Нет</span><span class="sxs-lookup"><span data-stu-id="d548b-117">N</span></span>        |
| <span data-ttu-id="d548b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d548b-118">Value</span></span>        | [<span data-ttu-id="d548b-119">Формате</span><span class="sxs-lookup"><span data-stu-id="d548b-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d548b-120">Нет</span><span class="sxs-lookup"><span data-stu-id="d548b-120">N</span></span>   | <span data-ttu-id="d548b-121">Да</span><span class="sxs-lookup"><span data-stu-id="d548b-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d548b-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d548b-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d548b-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span><span class="sxs-lookup"><span data-stu-id="d548b-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="d548b-124">Имя внутреннего маркера для источника данных.</span><span class="sxs-lookup"><span data-stu-id="d548b-124">Internal token name for data source.</span></span> <span data-ttu-id="d548b-125">Первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d548b-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="d548b-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию</span><span class="sxs-lookup"><span data-stu-id="d548b-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="d548b-127">Имя атрибута источника данных.</span><span class="sxs-lookup"><span data-stu-id="d548b-127">Name of data source attribute.</span></span> <span data-ttu-id="d548b-128">Первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d548b-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="d548b-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="d548b-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d548b-130">Локализуемое строковое значение для атрибута.</span><span class="sxs-lookup"><span data-stu-id="d548b-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d548b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d548b-131">Remarks</span></span>

<span data-ttu-id="d548b-132">Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="d548b-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="d548b-133">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d548b-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="d548b-134">Проверка</span><span class="sxs-lookup"><span data-stu-id="d548b-134">Validation</span></span>

<dl>

[<span data-ttu-id="d548b-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="d548b-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d548b-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="d548b-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d548b-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="d548b-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d548b-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="d548b-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



