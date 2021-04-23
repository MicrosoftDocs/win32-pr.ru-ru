---
description: В \_ таблице хранения перечислены внедренные хранилища данных OLE. Это временная таблица, созданная только в том случае, если на нее ссылается инструкция SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Таблица _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909167"
---
# <a name="_storages-table"></a><span data-ttu-id="6248e-104">\_Таблица хранилищ</span><span class="sxs-lookup"><span data-stu-id="6248e-104">\_Storages Table</span></span>

<span data-ttu-id="6248e-105">В \_ таблице хранения перечислены внедренные хранилища данных OLE.</span><span class="sxs-lookup"><span data-stu-id="6248e-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="6248e-106">Это временная таблица, созданная только в том случае, если на нее ссылается инструкция SQL.</span><span class="sxs-lookup"><span data-stu-id="6248e-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="6248e-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="6248e-107">Column</span></span> | <span data-ttu-id="6248e-108">Type</span><span class="sxs-lookup"><span data-stu-id="6248e-108">Type</span></span>                 | <span data-ttu-id="6248e-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="6248e-109">Key</span></span> | <span data-ttu-id="6248e-110">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6248e-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="6248e-111">Имя</span><span class="sxs-lookup"><span data-stu-id="6248e-111">Name</span></span>   | [<span data-ttu-id="6248e-112">Text</span><span class="sxs-lookup"><span data-stu-id="6248e-112">Text</span></span>](text.md)     | <span data-ttu-id="6248e-113">Да</span><span class="sxs-lookup"><span data-stu-id="6248e-113">Y</span></span>   | <span data-ttu-id="6248e-114">Нет</span><span class="sxs-lookup"><span data-stu-id="6248e-114">N</span></span>        |
| <span data-ttu-id="6248e-115">Данные</span><span class="sxs-lookup"><span data-stu-id="6248e-115">Data</span></span>   | [<span data-ttu-id="6248e-116">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6248e-116">Binary</span></span>](binary.md) | <span data-ttu-id="6248e-117">Нет</span><span class="sxs-lookup"><span data-stu-id="6248e-117">N</span></span>   | <span data-ttu-id="6248e-118">Да</span><span class="sxs-lookup"><span data-stu-id="6248e-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6248e-119">Столбцы</span><span class="sxs-lookup"><span data-stu-id="6248e-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6248e-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="6248e-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="6248e-121">Уникальный ключ, определяющий хранилище.</span><span class="sxs-lookup"><span data-stu-id="6248e-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="6248e-122">Максимальная длина имени — 31 символ.</span><span class="sxs-lookup"><span data-stu-id="6248e-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="6248e-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="6248e-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="6248e-124">Неформатированные двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="6248e-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6248e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6248e-125">Remarks</span></span>

<span data-ttu-id="6248e-126">Чтобы добавить хранилище OLE в базу данных, создайте новую запись в \_ таблице хранилища и введите имя хранилища в столбец имя.</span><span class="sxs-lookup"><span data-stu-id="6248e-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="6248e-127">Используйте [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) для копирования данных в столбец данных этой записи.</span><span class="sxs-lookup"><span data-stu-id="6248e-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="6248e-128">Наконец, используйте [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , чтобы вставить запись в \_ таблицу хранилищ.</span><span class="sxs-lookup"><span data-stu-id="6248e-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="6248e-129">Данные не могут быть считаны из \_ таблицы хранилищ.</span><span class="sxs-lookup"><span data-stu-id="6248e-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="6248e-130">Однако \_ таблицу хранилищ можно запросить для проверки существования определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6248e-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="6248e-131">Это означает, что невозможно переместить OLE-хранилище из одной базы данных в другую.</span><span class="sxs-lookup"><span data-stu-id="6248e-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="6248e-132">Вместо этого необходимо импортировать исходный файл хранилища в новую базу данных. Чтобы удалить хранилище OLE, выберите запись, содержащую двоичные данные, установите для столбца данных в \_ таблице хранилища значение null, а затем обновите запись.</span><span class="sxs-lookup"><span data-stu-id="6248e-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="6248e-133">Другой способ — просто удалить запись с помощью [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) или простого SQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="6248e-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="6248e-134">Чтобы переименовать хранилище OLE, обновите столбец имени записи.</span><span class="sxs-lookup"><span data-stu-id="6248e-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="6248e-135">Если для этой таблицы размещается удержание с помощью SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="6248e-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="6248e-136">УДЕРЖАНИЕ) или добавление столбца с УДЕРЖАНИЕм, таблица должна быть освобождена с помощью функции FREE.</span><span class="sxs-lookup"><span data-stu-id="6248e-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="6248e-137">Хранилища не записываются, пока таблица не будет освобождена или зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="6248e-137">Storages are not written until the table has been released or committed.</span></span>

 

 



