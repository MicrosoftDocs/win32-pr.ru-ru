---
description: Таблица Мсипатчхеадерс содержит потоки заголовков двоичного обновления, используемые для проверки исправлений.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Таблица Мсипатчхеадерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264838"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="32d2c-103">Таблица Мсипатчхеадерс</span><span class="sxs-lookup"><span data-stu-id="32d2c-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="32d2c-104">Таблица Мсипатчхеадерс содержит потоки заголовков двоичного обновления, используемые для проверки исправлений.</span><span class="sxs-lookup"><span data-stu-id="32d2c-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="32d2c-105">Таблица Мсипатчхеадерс используется, если ключи длинных [таблиц файлов](file-table.md) приводят к сбою при создании потока заголовков исправлений в [таблице Patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="32d2c-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="32d2c-106">Это может быть вызвано ограничением имен потоков, описанным в разделе [ограничения по OLE для потоков](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="32d2c-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="32d2c-107">В этом случае таблица Patch может ссылаться на таблицу Мсипатчхеадерс для создания потока заголовков исправлений.</span><span class="sxs-lookup"><span data-stu-id="32d2c-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="32d2c-108">Таблица Мсипатчхеадерс содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="32d2c-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="32d2c-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="32d2c-109">Column</span></span>    | <span data-ttu-id="32d2c-110">Type</span><span class="sxs-lookup"><span data-stu-id="32d2c-110">Type</span></span>                         | <span data-ttu-id="32d2c-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="32d2c-111">Key</span></span> | <span data-ttu-id="32d2c-112">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="32d2c-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="32d2c-113">стреамреф</span><span class="sxs-lookup"><span data-stu-id="32d2c-113">StreamRef</span></span> | [<span data-ttu-id="32d2c-114">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="32d2c-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="32d2c-115">Да</span><span class="sxs-lookup"><span data-stu-id="32d2c-115">Y</span></span>   | <span data-ttu-id="32d2c-116">Нет</span><span class="sxs-lookup"><span data-stu-id="32d2c-116">N</span></span>        |
| <span data-ttu-id="32d2c-117">Header</span><span class="sxs-lookup"><span data-stu-id="32d2c-117">Header</span></span>    | [<span data-ttu-id="32d2c-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="32d2c-118">Binary</span></span>](binary.md)         | <span data-ttu-id="32d2c-119">Нет</span><span class="sxs-lookup"><span data-stu-id="32d2c-119">N</span></span>   | <span data-ttu-id="32d2c-120">Нет</span><span class="sxs-lookup"><span data-stu-id="32d2c-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="32d2c-121">Столбцы</span><span class="sxs-lookup"><span data-stu-id="32d2c-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="32d2c-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>стреамреф</span><span class="sxs-lookup"><span data-stu-id="32d2c-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="32d2c-123">Первичный ключ для таблицы, однозначно определяющий конкретный заголовок исправления.</span><span class="sxs-lookup"><span data-stu-id="32d2c-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="32d2c-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Заголовок</span><span class="sxs-lookup"><span data-stu-id="32d2c-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="32d2c-125">Этот столбец является заголовком двоичного обновления потока, используемого для проверки исправлений.</span><span class="sxs-lookup"><span data-stu-id="32d2c-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32d2c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32d2c-126">Remarks</span></span>

<span data-ttu-id="32d2c-127">Эта таблица обрабатывается [действием патчфилес](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="32d2c-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="32d2c-128">Эта таблица обычно добавляется в пакет установки путем преобразования из пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="32d2c-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="32d2c-129">Обычно он не создается непосредственно в установочном пакете.</span><span class="sxs-lookup"><span data-stu-id="32d2c-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="32d2c-130">Проверка</span><span class="sxs-lookup"><span data-stu-id="32d2c-130">Validation</span></span>

<dl>

[<span data-ttu-id="32d2c-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="32d2c-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="32d2c-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="32d2c-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="32d2c-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="32d2c-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



