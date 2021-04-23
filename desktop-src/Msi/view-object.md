---
description: Объект View представляет результирующий набор, полученный при обработке запроса с помощью метода OpenView объекта Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Просмотр объекта
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675745"
---
# <a name="view-object"></a><span data-ttu-id="2d691-103">Просмотр объекта</span><span class="sxs-lookup"><span data-stu-id="2d691-103">View object</span></span>

<span data-ttu-id="2d691-104">Объект **View** представляет результирующий набор, полученный при обработке запроса с помощью метода [**OpenView**](database-openview.md) объекта [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="2d691-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="2d691-105">Перед передачей данных запрос должен быть выполнен с помощью метода [**EXECUTE**](view-execute.md) , передавая ему все заменяемые параметры, обозначенные в строке запроса SQL.</span><span class="sxs-lookup"><span data-stu-id="2d691-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="2d691-106">Запрос может быть выполнен повторно с другими параметрами, если это необходимо, но только после освобождения результирующего набора путем выборки всех записей или путем вызова метода [**Close**](view-close.md) .</span><span class="sxs-lookup"><span data-stu-id="2d691-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="2d691-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2d691-107">Members</span></span>

<span data-ttu-id="2d691-108">Объект **представления** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d691-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="2d691-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2d691-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d691-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d691-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d691-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2d691-111">Methods</span></span>

<span data-ttu-id="2d691-112">Объект **представления** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="2d691-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="2d691-113">Метод</span><span class="sxs-lookup"><span data-stu-id="2d691-113">Method</span></span>                            | <span data-ttu-id="2d691-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2d691-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d691-115">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="2d691-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="2d691-116">Прерывает выполнение запроса и освобождает ресурсы базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d691-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="2d691-117">**Работать**</span><span class="sxs-lookup"><span data-stu-id="2d691-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="2d691-118">Использует маркер вопросительного знака для представления параметров в SQL-запросе.</span><span class="sxs-lookup"><span data-stu-id="2d691-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="2d691-119">Значения этих параметров передаются в качестве соответствующих полей записи параметра.</span><span class="sxs-lookup"><span data-stu-id="2d691-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="2d691-120">**Водит**</span><span class="sxs-lookup"><span data-stu-id="2d691-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="2d691-121">Возвращает объект [**Record**](record-object.md) , содержащий запрошенные данные столбца, если в результирующем наборе доступно больше строк; в противном случае возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="2d691-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="2d691-122">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="2d691-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="2d691-123">Возвращает ошибку проверки и имя столбца, для которого произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="2d691-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2d691-124">**Изменений**</span><span class="sxs-lookup"><span data-stu-id="2d691-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="2d691-125">Изменяет строку базы данных с измененным объектом [**записи**](record-object.md) , полученным методом [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="2d691-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="2d691-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d691-126">Properties</span></span>

<span data-ttu-id="2d691-127">Объект **представления** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="2d691-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="2d691-128">Свойство</span><span class="sxs-lookup"><span data-stu-id="2d691-128">Property</span></span>                                         | <span data-ttu-id="2d691-129">Описание</span><span class="sxs-lookup"><span data-stu-id="2d691-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d691-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="2d691-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="2d691-131">Возвращает объект [**Record**](record-object.md) , содержащий запрошенные сведения о каждом столбце в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="2d691-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d691-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2d691-132">Requirements</span></span>



| <span data-ttu-id="2d691-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2d691-133">Requirement</span></span> | <span data-ttu-id="2d691-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2d691-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d691-135">Версия</span><span class="sxs-lookup"><span data-stu-id="2d691-135">Version</span></span><br/> | <span data-ttu-id="2d691-136">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d691-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2d691-137">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d691-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2d691-138">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d691-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2d691-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2d691-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d691-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d691-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2d691-141">IID</span><span class="sxs-lookup"><span data-stu-id="2d691-141">IID</span></span><br/>     | <span data-ttu-id="2d691-142">IID \_ IView определен как 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2d691-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="2d691-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d691-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d691-144">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="2d691-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




