---
description: ICE06 проверяет каждую таблицу, чтобы убедиться, что все столбцы, перечисленные в \_ таблице проверки, присутствуют в таблице. Если таблица не существует, все \_ записи проверки для этой таблицы игнорируются.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998804"
---
# <a name="ice06"></a><span data-ttu-id="0b3df-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="0b3df-104">ICE06</span></span>

<span data-ttu-id="0b3df-105">ICE06 проверяет каждую таблицу, чтобы убедиться, что все столбцы, перечисленные в [ \_ таблице проверки](-validation-table.md) , присутствуют в таблице.</span><span class="sxs-lookup"><span data-stu-id="0b3df-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="0b3df-106">Если таблица не существует, все \_ записи проверки для этой таблицы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="0b3df-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="0b3df-107">Целью ICE06 является обнаружение экземпляров, в которых автор пытается использовать новую \_ таблицу проверки, отражающую изменение схемы со старой базой данных, которая не была обновлена.</span><span class="sxs-lookup"><span data-stu-id="0b3df-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="0b3df-108">ICE06 также обнаруживает обратную \_ таблицу старой таблицы проверки, используемой в измененной базе данных.</span><span class="sxs-lookup"><span data-stu-id="0b3df-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="0b3df-109">Обратите внимание, что внутренняя проверка, выполняемая [ICE03](ice03.md) , перехватывает экземпляр столбца таблицы, не определенный в \_ таблице проверки, указанной в каталоге Columns.</span><span class="sxs-lookup"><span data-stu-id="0b3df-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="0b3df-110">Таким образом, использование ICE03 и ICE06 гарантирует тестирование каждого столбца в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0b3df-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="0b3df-111">Результат</span><span class="sxs-lookup"><span data-stu-id="0b3df-111">Result</span></span>

<span data-ttu-id="0b3df-112">ICE06 отправляет сообщение об ошибке, если в таблице проверки определен столбец таблицы \_ , не указанный в \_ таблице Columns.</span><span class="sxs-lookup"><span data-stu-id="0b3df-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="0b3df-113">Пример</span><span class="sxs-lookup"><span data-stu-id="0b3df-113">Example</span></span>

<span data-ttu-id="0b3df-114">В следующем примере ICE06 отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="0b3df-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="0b3df-115">Столбец: версия таблицы: ModuleSignature не определен в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0b3df-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="0b3df-116">[ \_ Таблица проверки](-validation-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="0b3df-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="0b3df-117">Таблица</span><span class="sxs-lookup"><span data-stu-id="0b3df-117">Table</span></span>           | <span data-ttu-id="0b3df-118">Столбец</span><span class="sxs-lookup"><span data-stu-id="0b3df-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="0b3df-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="0b3df-119">ModuleSignature</span></span> | <span data-ttu-id="0b3df-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="0b3df-120">ModuleID</span></span> |
| <span data-ttu-id="0b3df-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="0b3df-121">ModuleSignature</span></span> | <span data-ttu-id="0b3df-122">Версия</span><span class="sxs-lookup"><span data-stu-id="0b3df-122">Version</span></span>  |



 

<span data-ttu-id="0b3df-123">[ \_ Таблица Columns](-columns-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="0b3df-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="0b3df-124">Таблица</span><span class="sxs-lookup"><span data-stu-id="0b3df-124">Table</span></span>           | <span data-ttu-id="0b3df-125">number</span><span class="sxs-lookup"><span data-stu-id="0b3df-125">Number</span></span> | <span data-ttu-id="0b3df-126">name</span><span class="sxs-lookup"><span data-stu-id="0b3df-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="0b3df-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="0b3df-127">ModuleSignature</span></span> | <span data-ttu-id="0b3df-128">1</span><span class="sxs-lookup"><span data-stu-id="0b3df-128">1</span></span>      | <span data-ttu-id="0b3df-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="0b3df-129">ModuleID</span></span> |



 

<span data-ttu-id="0b3df-130">Столбец Version таблицы ModuleSignature отсутствует в базе данных или указан в \_ таблице Columns.</span><span class="sxs-lookup"><span data-stu-id="0b3df-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b3df-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0b3df-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b3df-132">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="0b3df-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



