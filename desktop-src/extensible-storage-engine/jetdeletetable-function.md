---
description: Дополнительные сведения о функции Жетделететабле
title: Функция Жетделететабле
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713141"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="3371e-103">Функция Жетделететабле</span><span class="sxs-lookup"><span data-stu-id="3371e-103">JetDeleteTable Function</span></span>


<span data-ttu-id="3371e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3371e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="3371e-105">Функция Жетделететабле</span><span class="sxs-lookup"><span data-stu-id="3371e-105">JetDeleteTable Function</span></span>

<span data-ttu-id="3371e-106">Функция **жетделететабле** удаляет таблицу в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="3371e-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="3371e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3371e-107">Parameters</span></span>

<span data-ttu-id="3371e-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="3371e-108">*sesid*</span></span>

<span data-ttu-id="3371e-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="3371e-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="3371e-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="3371e-110">*dbid*</span></span>

<span data-ttu-id="3371e-111">Идентификатор базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="3371e-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="3371e-112">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="3371e-112">*szTableName*</span></span>

<span data-ttu-id="3371e-113">Имя таблицы для удаления.</span><span class="sxs-lookup"><span data-stu-id="3371e-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="3371e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3371e-114">Return Value</span></span>

<span data-ttu-id="3371e-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="3371e-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3371e-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3371e-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3371e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3371e-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="3371e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3371e-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3371e-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3371e-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3371e-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3371e-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3371e-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="3371e-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="3371e-122">Предпринята попытка удалить таблицу, в то время как другой сеанс имеет идентификатор открытой таблицы (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) с <a href="gg294118(v=exchg.10).md">жетопентабле</a> или <a href="gg269193(v=exchg.10).md">жетдупкурсор</a>.</span><span class="sxs-lookup"><span data-stu-id="3371e-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3371e-123">Таблица JET_errCannotDeletetemporary</span><span class="sxs-lookup"><span data-stu-id="3371e-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="3371e-124">Была предпринята попытка удалить временную таблицу.</span><span class="sxs-lookup"><span data-stu-id="3371e-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="3371e-125">Временная таблица автоматически удаляется, когда она закрывается с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>.</span><span class="sxs-lookup"><span data-stu-id="3371e-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3371e-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="3371e-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="3371e-127">Предпринята попытка удалить таблицу шаблонов, то есть таблицу, из которой может быть унаследована инструкция DDL.</span><span class="sxs-lookup"><span data-stu-id="3371e-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="3371e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3371e-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3371e-129"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="3371e-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3371e-130">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3371e-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3371e-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3371e-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3371e-132">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3371e-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3371e-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3371e-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3371e-134">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3371e-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3371e-135"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="3371e-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3371e-136">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3371e-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3371e-137"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="3371e-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3371e-138">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3371e-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3371e-139"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="3371e-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3371e-140">Реализуется как <strong>жетделететаблев</strong> (Юникод) и <strong>жетделететаблеа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3371e-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3371e-141">См. также:</span><span class="sxs-lookup"><span data-stu-id="3371e-141">See Also</span></span>

[<span data-ttu-id="3371e-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="3371e-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="3371e-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3371e-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3371e-144">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="3371e-144">JetCloseTable</span></span>](./jetclosetable-function.md)
