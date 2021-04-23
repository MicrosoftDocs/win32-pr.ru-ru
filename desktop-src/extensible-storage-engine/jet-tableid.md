---
description: 'Дополнительные сведения: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693354"
---
# <a name="jet_tableid"></a><span data-ttu-id="b5a18-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5a18-103">JET_TABLEID</span></span>


<span data-ttu-id="b5a18-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b5a18-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="b5a18-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5a18-105">JET_TABLEID</span></span>

<span data-ttu-id="b5a18-106">JET_TABLEID тип данных содержит указатель на курсор базы данных, используемый для вызова API JET.</span><span class="sxs-lookup"><span data-stu-id="b5a18-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="b5a18-107">Курсор можно использовать только с сеансом, который использовался для открытия этого курсора.</span><span class="sxs-lookup"><span data-stu-id="b5a18-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="b5a18-108">Типы данных</span><span class="sxs-lookup"><span data-stu-id="b5a18-108">Data Types</span></span>

<span data-ttu-id="b5a18-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5a18-109">JET_TABLEID</span></span>

<span data-ttu-id="b5a18-110">Для указания недопустимого маркера курсора можно использовать **значение NULL** или [JET_tableidNil](./invalid-handle-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="b5a18-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="b5a18-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5a18-111">Remarks</span></span>

<span data-ttu-id="b5a18-112">Курсор управляет использованием таблицы для ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="b5a18-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="b5a18-113">Курсор может выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b5a18-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="b5a18-114">Просмотр записей</span><span class="sxs-lookup"><span data-stu-id="b5a18-114">Scan records</span></span>

  - <span data-ttu-id="b5a18-115">Поиск записей</span><span class="sxs-lookup"><span data-stu-id="b5a18-115">Search for records</span></span>

  - <span data-ttu-id="b5a18-116">Выберите эффективный порядок сортировки и видимость этих записей</span><span class="sxs-lookup"><span data-stu-id="b5a18-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="b5a18-117">Создание, обновление и удаление записей</span><span class="sxs-lookup"><span data-stu-id="b5a18-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="b5a18-118">Изменение схемы таблицы</span><span class="sxs-lookup"><span data-stu-id="b5a18-118">Modify the schema of the table</span></span>

<span data-ttu-id="b5a18-119">Поддерживаемые функциональные возможности курсора могут изменяться по мере изменения состояния или типа базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="b5a18-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="b5a18-120">Например, временная таблица может запретить поиск данных при открытии с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="b5a18-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="b5a18-121">Курсор всегда полностью подключен к базовой таблице и взаимодействует с данными напрямую без кэширования.</span><span class="sxs-lookup"><span data-stu-id="b5a18-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="b5a18-122">Почти все основные функции ISAM, предоставляемые этим ядром СУБД, работают с курсором.</span><span class="sxs-lookup"><span data-stu-id="b5a18-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="b5a18-123">Курсор можно создать с помощью [жетопентабле](./jetopentable-function.md) или [жетопентемптабле](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5a18-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="b5a18-124">Курсор можно дублировать с помощью [жетдупкурсор](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5a18-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="b5a18-125">Курсор можно явно закрыть с помощью [жетклосетабле](./jetclosetable-function.md) или неявно закрыть с помощью [жетендсессион](./jetendsession-function.md) или [жеттерм](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5a18-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="b5a18-126">Курсор также может быть неявно закрыт [жетроллбакк](./jetrollback-function.md) , если он был открыт в транзакции, которая была прервана.</span><span class="sxs-lookup"><span data-stu-id="b5a18-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="b5a18-127">Максимальное количество курсоров, которые могут быть созданы за один раз, управляется [JET_paramMaxCursors](./resource-parameters.md), которые можно настроить с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5a18-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="b5a18-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b5a18-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5a18-129"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b5a18-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a18-130">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b5a18-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a18-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b5a18-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a18-132">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b5a18-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a18-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b5a18-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a18-134">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b5a18-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b5a18-135">См. также:</span><span class="sxs-lookup"><span data-stu-id="b5a18-135">See Also</span></span>

[<span data-ttu-id="b5a18-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="b5a18-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="b5a18-137">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="b5a18-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b5a18-138">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="b5a18-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="b5a18-139">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="b5a18-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="b5a18-140">жетопентабле</span><span class="sxs-lookup"><span data-stu-id="b5a18-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="b5a18-141">жетопентемптабле</span><span class="sxs-lookup"><span data-stu-id="b5a18-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="b5a18-142">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="b5a18-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b5a18-143">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="b5a18-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="b5a18-144">жеттерм</span><span class="sxs-lookup"><span data-stu-id="b5a18-144">JetTerm</span></span>](./jetterm-function.md)
