---
description: Спецификация примера состоит в том, что данные учетной записи пользователя считываются из пользовательской таблицы в базе данных установки и не жестко запрограммированы в настраиваемом действии.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Добавление пользовательской таблицы Кустомусераккаунтс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650742"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="6c790-103">Добавление пользовательской таблицы Кустомусераккаунтс</span><span class="sxs-lookup"><span data-stu-id="6c790-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="6c790-104">Спецификация примера состоит в том, что данные учетной записи пользователя считываются из пользовательской таблицы в базе данных установки и не жестко запрограммированы в настраиваемом действии.</span><span class="sxs-lookup"><span data-stu-id="6c790-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="6c790-105">Добавьте пользовательскую таблицу в образец базы данных установки с именем Кустомусераккаунтс, чтобы сохранить сведения об учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c790-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="6c790-106">Пример добавления настраиваемой таблицы см. в статьях [примеры запросов к базам данных с использованием SQL и скрипта](examples-of-database-queries-using-sql-and-script.md) .</span><span class="sxs-lookup"><span data-stu-id="6c790-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="6c790-107">Используйте следующую схему для таблицы Кустомусераккаунтс.</span><span class="sxs-lookup"><span data-stu-id="6c790-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="6c790-108">Описание типов столбцов см. в разделе [Формат определения столбца](column-definition-format.md) .</span><span class="sxs-lookup"><span data-stu-id="6c790-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="6c790-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="6c790-109">Column</span></span>     | <span data-ttu-id="6c790-110">Type</span><span class="sxs-lookup"><span data-stu-id="6c790-110">Type</span></span> | <span data-ttu-id="6c790-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="6c790-111">Key</span></span> | <span data-ttu-id="6c790-112">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6c790-112">Nullable</span></span> | <span data-ttu-id="6c790-113">Описание</span><span class="sxs-lookup"><span data-stu-id="6c790-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c790-114">UserName</span><span class="sxs-lookup"><span data-stu-id="6c790-114">UserName</span></span>   | <span data-ttu-id="6c790-115">s72</span><span class="sxs-lookup"><span data-stu-id="6c790-115">s72</span></span>  | <span data-ttu-id="6c790-116">Да</span><span class="sxs-lookup"><span data-stu-id="6c790-116">Y</span></span>   | <span data-ttu-id="6c790-117">Нет</span><span class="sxs-lookup"><span data-stu-id="6c790-117">N</span></span>        | <span data-ttu-id="6c790-118">Имя создаваемой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c790-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6c790-119">Пароль</span><span class="sxs-lookup"><span data-stu-id="6c790-119">Password</span></span>   | <span data-ttu-id="6c790-120">s72</span><span class="sxs-lookup"><span data-stu-id="6c790-120">s72</span></span>  |     | <span data-ttu-id="6c790-121">Нет</span><span class="sxs-lookup"><span data-stu-id="6c790-121">N</span></span>        | <span data-ttu-id="6c790-122">Имя свойства, содержащего пароль для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6c790-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="6c790-123">Это [общедоступное свойство](public-properties.md) , заданное в командной строке или с помощью [элемента управления](edit-control.md) "поле ввода" в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="6c790-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="6c790-124">Этот элемент управления "поле ввода" должен иметь [атрибут управления паролями](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="6c790-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="6c790-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6c790-125">Attributes</span></span> | <span data-ttu-id="6c790-126">i4</span><span class="sxs-lookup"><span data-stu-id="6c790-126">i4</span></span>   |     | <span data-ttu-id="6c790-127">Да</span><span class="sxs-lookup"><span data-stu-id="6c790-127">Y</span></span>        | <span data-ttu-id="6c790-128">Атрибуты для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6c790-128">Attributes for account.</span></span> <span data-ttu-id="6c790-129">Они определены как значения **типа DWORD** для \_ элемента flags USRI1 в \_ структуре пользователя \_ 1.</span><span class="sxs-lookup"><span data-stu-id="6c790-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="6c790-130">После добавления таблицы Кустомусераккаунтс в базу данных эту таблицу можно изменить с помощью Orca, редактора таблиц, поставляемого с пакетом SDK установщик Windows, или другого редактора.</span><span class="sxs-lookup"><span data-stu-id="6c790-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="6c790-131">Введите следующую запись в таблицу Кустомусераккаунтс, чтобы создать защищенную паролем учетную запись пользователя для пользователя с именем TestUser.</span><span class="sxs-lookup"><span data-stu-id="6c790-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="6c790-132">Обратите внимание, что 512 — это числовое значение для \_ обычной \_ учетной записи УФ.</span><span class="sxs-lookup"><span data-stu-id="6c790-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="6c790-133">Таблица Кустомусераккаунтс</span><span class="sxs-lookup"><span data-stu-id="6c790-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="6c790-134">UserName</span><span class="sxs-lookup"><span data-stu-id="6c790-134">UserName</span></span> | <span data-ttu-id="6c790-135">Пароль</span><span class="sxs-lookup"><span data-stu-id="6c790-135">Password</span></span>         | <span data-ttu-id="6c790-136">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6c790-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="6c790-137">TestUser</span><span class="sxs-lookup"><span data-stu-id="6c790-137">TestUser</span></span> | <span data-ttu-id="6c790-138">тестусерпассворд</span><span class="sxs-lookup"><span data-stu-id="6c790-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="6c790-139">512</span><span class="sxs-lookup"><span data-stu-id="6c790-139">512</span></span>        |



 

<span data-ttu-id="6c790-140">Добавьте следующие записи в \_ таблицу проверки для настраиваемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="6c790-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="6c790-141">\_Таблица проверки</span><span class="sxs-lookup"><span data-stu-id="6c790-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="6c790-142">Таблица</span><span class="sxs-lookup"><span data-stu-id="6c790-142">Table</span></span>              | <span data-ttu-id="6c790-143">Столбец</span><span class="sxs-lookup"><span data-stu-id="6c790-143">Column</span></span>     | <span data-ttu-id="6c790-144">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6c790-144">Nullable</span></span> | <span data-ttu-id="6c790-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="6c790-145">MinValue</span></span> | <span data-ttu-id="6c790-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6c790-146">MaxValue</span></span>   | <span data-ttu-id="6c790-147">кэйтабле</span><span class="sxs-lookup"><span data-stu-id="6c790-147">KeyTable</span></span> | <span data-ttu-id="6c790-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="6c790-148">KeyColumn</span></span> | <span data-ttu-id="6c790-149">Категория</span><span class="sxs-lookup"><span data-stu-id="6c790-149">Category</span></span>                     | <span data-ttu-id="6c790-150">Присвойте параметру</span><span class="sxs-lookup"><span data-stu-id="6c790-150">Set</span></span> | <span data-ttu-id="6c790-151">Описание</span><span class="sxs-lookup"><span data-stu-id="6c790-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="6c790-152">кустомусераккаунтс</span><span class="sxs-lookup"><span data-stu-id="6c790-152">CustomUserAccounts</span></span> | <span data-ttu-id="6c790-153">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="6c790-153">UserName</span></span>   | <span data-ttu-id="6c790-154">Нет</span><span class="sxs-lookup"><span data-stu-id="6c790-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="6c790-155">Text</span><span class="sxs-lookup"><span data-stu-id="6c790-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="6c790-156">кустомусераккаунтс</span><span class="sxs-lookup"><span data-stu-id="6c790-156">CustomUserAccounts</span></span> | <span data-ttu-id="6c790-157">Пароль</span><span class="sxs-lookup"><span data-stu-id="6c790-157">Password</span></span>   | <span data-ttu-id="6c790-158">Нет</span><span class="sxs-lookup"><span data-stu-id="6c790-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="6c790-159">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6c790-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="6c790-160">кустомусераккаунтс</span><span class="sxs-lookup"><span data-stu-id="6c790-160">CustomUserAccounts</span></span> | <span data-ttu-id="6c790-161">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6c790-161">Attributes</span></span> | <span data-ttu-id="6c790-162">Да</span><span class="sxs-lookup"><span data-stu-id="6c790-162">Y</span></span>        | <span data-ttu-id="6c790-163">0</span><span class="sxs-lookup"><span data-stu-id="6c790-163">0</span></span>        | <span data-ttu-id="6c790-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="6c790-164">2147483647</span></span> |          |           | <span data-ttu-id="6c790-165">null</span><span class="sxs-lookup"><span data-stu-id="6c790-165">null</span></span>                         |     |             |



 

<span data-ttu-id="6c790-166">Продолжайте [Создание актионтекст и таблиц ошибок](authoring-the-actiontext-and-error-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6c790-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



