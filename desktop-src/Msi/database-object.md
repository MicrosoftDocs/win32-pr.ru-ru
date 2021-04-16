---
description: Объект базы данных обращается к базе данных установщика.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Объект базы данных
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669351"
---
# <a name="database-object"></a><span data-ttu-id="815b3-103">Объект базы данных</span><span class="sxs-lookup"><span data-stu-id="815b3-103">Database object</span></span>

<span data-ttu-id="815b3-104">Объект **базы данных** обращается к базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="815b3-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="815b3-105">Объект **базы данных** освобождается, когда либо выводится из области, либо когда связанная с ним объектная переменная имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="815b3-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="815b3-106">Метод [**commit**](database-commit.md) должен быть вызван до освобождения объекта **базы данных** для записи всех постоянных изменений.</span><span class="sxs-lookup"><span data-stu-id="815b3-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="815b3-107">Если метод **commit** не вызывается, установщик выполняет неявный откат при уничтожении объекта.</span><span class="sxs-lookup"><span data-stu-id="815b3-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="815b3-108">Для доступа к данным клиент может использовать следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="815b3-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="815b3-109">**Запрос последовательности API**</span><span class="sxs-lookup"><span data-stu-id="815b3-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="815b3-110">Получите объект **базы данных** , вызвав [**Опендатабасе**](installer-opendatabase.md) или объект [**установщика**](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="815b3-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="815b3-111">Запустите запрос с помощью строки SQL, вызвав метод [**OpenView**](database-openview.md) объекта **Database** .</span><span class="sxs-lookup"><span data-stu-id="815b3-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="815b3-112">Задайте параметры запроса в объекте [**Record**](record-object.md) и выполните запрос к базе данных, вызвав метод [**EXECUTE**](view-execute.md) объекта [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="815b3-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="815b3-113">В результате получается результат, который можно извлечь или обновить.</span><span class="sxs-lookup"><span data-stu-id="815b3-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="815b3-114">Повторно вызывайте метод [**Fetch**](view-fetch.md) объекта [**представления**](view-object.md) , чтобы вернуть объекты [**записи**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="815b3-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="815b3-115">Обновите строки базы данных объекта [**записи**](record-object.md) , полученные методом [**Fetch**](view-fetch.md) , с помощью метода [**Modify**](view-modify.md) объекта [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="815b3-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="815b3-116">Выпустите запрос и все невыбранные записи, вызвав метод [**Close**](view-close.md) объекта [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="815b3-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="815b3-117">Сохраните обновления базы данных, вызвав метод [**commit**](database-commit.md) объекта **Database** .</span><span class="sxs-lookup"><span data-stu-id="815b3-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="815b3-118">Элементы</span><span class="sxs-lookup"><span data-stu-id="815b3-118">Members</span></span>

<span data-ttu-id="815b3-119">Объект **базы данных** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="815b3-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="815b3-120">Методы</span><span class="sxs-lookup"><span data-stu-id="815b3-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="815b3-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="815b3-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="815b3-122">Методы</span><span class="sxs-lookup"><span data-stu-id="815b3-122">Methods</span></span>

<span data-ttu-id="815b3-123">Объект **базы данных** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="815b3-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="815b3-124">Метод</span><span class="sxs-lookup"><span data-stu-id="815b3-124">Method</span></span>                                                                    | <span data-ttu-id="815b3-125">Описание</span><span class="sxs-lookup"><span data-stu-id="815b3-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="815b3-126">**апплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="815b3-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="815b3-127">Применяет преобразование к этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="815b3-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="815b3-128">**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="815b3-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="815b3-129">Завершает постоянную форму базы данных.</span><span class="sxs-lookup"><span data-stu-id="815b3-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="815b3-130">**креатетрансформсуммаринфо**</span><span class="sxs-lookup"><span data-stu-id="815b3-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="815b3-131">Создает и заполняет поток сводных данных существующего файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="815b3-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="815b3-132">**енаблеуипревиев**</span><span class="sxs-lookup"><span data-stu-id="815b3-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="815b3-133">Упрощает создание диалоговых окон и объявлений, предоставляя поддержку, необходимую для просмотра диалоговых окон пользовательского интерфейса, хранящихся в базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="815b3-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="815b3-134">**Экспорт**</span><span class="sxs-lookup"><span data-stu-id="815b3-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="815b3-135">Копирует структуру и данные из указанной таблицы в текстовый файл архива.</span><span class="sxs-lookup"><span data-stu-id="815b3-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="815b3-136">**Преобразование**</span><span class="sxs-lookup"><span data-stu-id="815b3-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="815b3-137">Создает преобразование.</span><span class="sxs-lookup"><span data-stu-id="815b3-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="815b3-138">**Импорт**</span><span class="sxs-lookup"><span data-stu-id="815b3-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="815b3-139">Импортирует таблицу базы данных из текстового файла архива.</span><span class="sxs-lookup"><span data-stu-id="815b3-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="815b3-140">**AutoMerge**</span><span class="sxs-lookup"><span data-stu-id="815b3-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="815b3-141">Объединяет эталонную базу данных с базовой базой данных.</span><span class="sxs-lookup"><span data-stu-id="815b3-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="815b3-142">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="815b3-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="815b3-143">Возвращает объект [**представления**](view-object.md) , представляющий запрос, заданный строкой SQL.</span><span class="sxs-lookup"><span data-stu-id="815b3-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="815b3-144">Свойства</span><span class="sxs-lookup"><span data-stu-id="815b3-144">Properties</span></span>

<span data-ttu-id="815b3-145">У объекта **базы данных** есть эти свойства.</span><span class="sxs-lookup"><span data-stu-id="815b3-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="815b3-146">Свойство</span><span class="sxs-lookup"><span data-stu-id="815b3-146">Property</span></span>                                                                               | <span data-ttu-id="815b3-147">Описание</span><span class="sxs-lookup"><span data-stu-id="815b3-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="815b3-148">**датабасестате**</span><span class="sxs-lookup"><span data-stu-id="815b3-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="815b3-149">Возвращает состояние сохраняемости базы данных.</span><span class="sxs-lookup"><span data-stu-id="815b3-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="815b3-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="815b3-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="815b3-151">Возвращает объект [**Record**](record-object.md) , содержащий имя таблицы и имена столбцов (в том состоят первичные ключи).</span><span class="sxs-lookup"><span data-stu-id="815b3-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="815b3-152">**SummaryInformation (объект Database)**</span><span class="sxs-lookup"><span data-stu-id="815b3-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="815b3-153">Возвращает объект [**суммаринфо**](summaryinfo-object.md) , который может использоваться для проверки, обновления и добавления свойств в поток сводных данных.</span><span class="sxs-lookup"><span data-stu-id="815b3-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="815b3-154">**таблеперсистент**</span><span class="sxs-lookup"><span data-stu-id="815b3-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="815b3-155">Возвращает состояние сохраняемости таблицы.</span><span class="sxs-lookup"><span data-stu-id="815b3-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="815b3-156">Требования</span><span class="sxs-lookup"><span data-stu-id="815b3-156">Requirements</span></span>



| <span data-ttu-id="815b3-157">Требование</span><span class="sxs-lookup"><span data-stu-id="815b3-157">Requirement</span></span> | <span data-ttu-id="815b3-158">Значение</span><span class="sxs-lookup"><span data-stu-id="815b3-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="815b3-159">Версия</span><span class="sxs-lookup"><span data-stu-id="815b3-159">Version</span></span><br/> | <span data-ttu-id="815b3-160">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="815b3-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="815b3-161">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="815b3-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="815b3-162">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="815b3-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="815b3-163">DLL</span><span class="sxs-lookup"><span data-stu-id="815b3-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="815b3-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="815b3-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="815b3-165">IID</span><span class="sxs-lookup"><span data-stu-id="815b3-165">IID</span></span><br/>     | <span data-ttu-id="815b3-166">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="815b3-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="815b3-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="815b3-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815b3-168">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="815b3-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




