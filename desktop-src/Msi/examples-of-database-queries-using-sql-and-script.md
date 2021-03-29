---
description: Пример использования запросов к базе данных, основанных на сценариях, предоставляется в установщик Windows пакете средств разработки программного обеспечения (SDK) в качестве служебной WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Примеры запросов к базе данных с помощью SQL и скрипта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812869"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="2268a-103">Примеры запросов к базе данных с помощью SQL и скрипта</span><span class="sxs-lookup"><span data-stu-id="2268a-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="2268a-104">Пример использования запросов к базе данных, управляемых сценариями, предоставляется в пакете SDK для [установщика](platform-sdk-components-for-windows-installer-developers.md) Windows в качестве служебной WiRunSQL.vbs.</span><span class="sxs-lookup"><span data-stu-id="2268a-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="2268a-105">Эта служебная программа обрабатывает запросы к базе данных с помощью установщик Windows версии SQL, описанной в разделе [синтаксис SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2268a-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="2268a-106">**Удаление записи из таблицы**</span><span class="sxs-lookup"><span data-stu-id="2268a-106">**Delete a record from a table**</span></span>

<span data-ttu-id="2268a-107">Следующая командная строка удаляет запись с основным ключом Красного из таблицы [Features](feature-table.md) базы данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="2268a-108">**Cscript WiRunSQL.vbs Test.msi "удалить из \` компонента \` , где находится \` функция \` . \` Функция \` = ' Red ' "**</span><span class="sxs-lookup"><span data-stu-id="2268a-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="2268a-109">**Добавление таблицы в базу данных**</span><span class="sxs-lookup"><span data-stu-id="2268a-109">**Add a table to a database**</span></span>

<span data-ttu-id="2268a-110">Следующая командная строка добавляет таблицу [Directory](directory-table.md) в базу данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="2268a-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory \` ( \` каталог \` char (72) NOT NULL, \` \_ родительский каталог \` char (72), \` дефаултдир \` char (255) не NULL локализуемый каталог первичного ключа \` \` )"**</span><span class="sxs-lookup"><span data-stu-id="2268a-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="2268a-112">**Удаление таблицы из базы данных**</span><span class="sxs-lookup"><span data-stu-id="2268a-112">**Remove a table from a database**</span></span>

<span data-ttu-id="2268a-113">Следующая командная строка удаляет таблицу [компонентов](feature-table.md) из базы данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="2268a-114">**Cscript WiRunSQL.vbs Test.msi "функция удаления \` таблицы \` "**</span><span class="sxs-lookup"><span data-stu-id="2268a-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="2268a-115">**Добавление нового столбца в таблицу**</span><span class="sxs-lookup"><span data-stu-id="2268a-115">**Add a new column to a table**</span></span>

<span data-ttu-id="2268a-116">Следующая командная строка добавляет Тестовый столбец в таблицу [CustomAction](customaction-table.md) базы данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="2268a-117">**CScript WiRunSQL.vbs Test.msi "Изменение настраиваемого \` CustomAction, \` Добавление \` тестового \` целого числа"**</span><span class="sxs-lookup"><span data-stu-id="2268a-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="2268a-118">**Вставить новую запись в таблицу**</span><span class="sxs-lookup"><span data-stu-id="2268a-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="2268a-119">Следующая командная строка вставляет новую запись в таблицу [Features](feature-table.md) базы данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="2268a-120">**Cscript WiRunSQL.vbs Test.msi "функция вставки в \` функцию \` (функция) \` \` . \` Функция \` , \` функция \` . \` \_Родительская функция \` , \` функция \` . \` Название \` , \` функция \` . \` Описание \` , \` функция \` . \` Отображение \` , \` функция \` . \` Уровень \` , \` функция \` . \` Каталог \_ \` , \` функция \` . \` Attributes \` ) Values ("теннис", "Спорт", "теннис", "турнира", 25, 3, "спортдир", 2) "**</span><span class="sxs-lookup"><span data-stu-id="2268a-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="2268a-121">В таблицу [Features](feature-table.md) компонента Test.msi вставляется следующая запись.</span><span class="sxs-lookup"><span data-stu-id="2268a-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="2268a-122">[Функция](feature-table.md) Таблица</span><span class="sxs-lookup"><span data-stu-id="2268a-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="2268a-123">Функция</span><span class="sxs-lookup"><span data-stu-id="2268a-123">Feature</span></span> | <span data-ttu-id="2268a-124">\_Родительский компонент функции</span><span class="sxs-lookup"><span data-stu-id="2268a-124">Feature\_Parent</span></span> | <span data-ttu-id="2268a-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2268a-125">Title</span></span>  | <span data-ttu-id="2268a-126">Описание</span><span class="sxs-lookup"><span data-stu-id="2268a-126">Description</span></span> | <span data-ttu-id="2268a-127">Отображение</span><span class="sxs-lookup"><span data-stu-id="2268a-127">Display</span></span> | <span data-ttu-id="2268a-128">Level</span><span class="sxs-lookup"><span data-stu-id="2268a-128">Level</span></span> | <span data-ttu-id="2268a-129">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="2268a-129">Directory\_</span></span> | <span data-ttu-id="2268a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2268a-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="2268a-131">Теннис</span><span class="sxs-lookup"><span data-stu-id="2268a-131">Tennis</span></span>  | <span data-ttu-id="2268a-132">Спорт</span><span class="sxs-lookup"><span data-stu-id="2268a-132">Sport</span></span>           | <span data-ttu-id="2268a-133">Теннис</span><span class="sxs-lookup"><span data-stu-id="2268a-133">Tennis</span></span> | <span data-ttu-id="2268a-134">Турнира</span><span class="sxs-lookup"><span data-stu-id="2268a-134">Tournament</span></span>  | <span data-ttu-id="2268a-135">25</span><span class="sxs-lookup"><span data-stu-id="2268a-135">25</span></span>      | <span data-ttu-id="2268a-136">3</span><span class="sxs-lookup"><span data-stu-id="2268a-136">3</span></span>     | <span data-ttu-id="2268a-137">спортдир</span><span class="sxs-lookup"><span data-stu-id="2268a-137">SPORTDIR</span></span>    | <span data-ttu-id="2268a-138">2</span><span class="sxs-lookup"><span data-stu-id="2268a-138">2</span></span>          |



 

<span data-ttu-id="2268a-139">Обратите внимание, что двоичные данные не могут быть вставлены в таблицу непосредственно с помощью инструкций INSERT или UPDATE в SQL-запросах.</span><span class="sxs-lookup"><span data-stu-id="2268a-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="2268a-140">Дополнительные сведения см. [в разделе Добавление двоичных данных в таблицу с помощью SQL](adding-binary-data-to-a-table-using-sql.md).</span><span class="sxs-lookup"><span data-stu-id="2268a-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="2268a-141">**Изменение существующей записи в таблице**</span><span class="sxs-lookup"><span data-stu-id="2268a-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="2268a-142">Следующая командная строка изменяет существующее значение в поле Title на «производительность».</span><span class="sxs-lookup"><span data-stu-id="2268a-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="2268a-143">Обновленная запись имеет "искусство" в качестве первичного ключа и находится в таблице функций базы данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="2268a-144">**Cscript WiRunSQL.vbs Test.msi "обновление \` \` компонента набора \` функций \` . \` Title \` = ' производительность ' \` , где функция \` . \` Feature \` = ' искусство ' '**</span><span class="sxs-lookup"><span data-stu-id="2268a-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="2268a-145">**Выберите группу записей**</span><span class="sxs-lookup"><span data-stu-id="2268a-145">**Select a group of records**</span></span>

<span data-ttu-id="2268a-146">Следующая командная строка выбирает имя и тип всех элементов управления, принадлежащих к Еррордиалог в базе данных Test.msi.</span><span class="sxs-lookup"><span data-stu-id="2268a-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="2268a-147">**CScript WiRunSQL.vbs Test.msi "выберите \` элемент управления \` , \` введите \` из \` элемента управления, \` где \` DIALOG \_ \` = ' еррордиалог '"**</span><span class="sxs-lookup"><span data-stu-id="2268a-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="2268a-148">**Хранение таблицы в памяти**</span><span class="sxs-lookup"><span data-stu-id="2268a-148">**Hold a table in memory**</span></span>

<span data-ttu-id="2268a-149">Следующая командная строка блокирует таблицу [компонентов](component-table.md) Test.msiной базы данных в памяти.</span><span class="sxs-lookup"><span data-stu-id="2268a-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="2268a-150">**CScript WiRunSQL.vbs Test.msi "изменение ТАБЛИЧного \` компонента \` хранения"**</span><span class="sxs-lookup"><span data-stu-id="2268a-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="2268a-151">**Освобождение таблицы в памяти**</span><span class="sxs-lookup"><span data-stu-id="2268a-151">**Free a table in memory**</span></span>

<span data-ttu-id="2268a-152">Следующая командная строка освобождает таблицу [Component](component-table.md) базы данных Test.msi из памяти.</span><span class="sxs-lookup"><span data-stu-id="2268a-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="2268a-153">**WiRunSQL.vbs CScript Test.msi "изменение \` компонента таблицы \` Free"**</span><span class="sxs-lookup"><span data-stu-id="2268a-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



