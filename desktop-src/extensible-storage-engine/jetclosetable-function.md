---
description: Дополнительные сведения о функции Жетклосетабле
title: Функция Жетклосетабле
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548159"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="1a75e-103">Функция Жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="1a75e-103">JetCloseTable Function</span></span>


<span data-ttu-id="1a75e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1a75e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="1a75e-105">Функция Жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="1a75e-105">JetCloseTable Function</span></span>

<span data-ttu-id="1a75e-106">Функция **жетклосетабле** закрывает открытую таблицу в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1a75e-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="1a75e-107">Таблица может быть временной или обычной таблицей.</span><span class="sxs-lookup"><span data-stu-id="1a75e-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="1a75e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a75e-108">Parameters</span></span>

<span data-ttu-id="1a75e-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="1a75e-109">*sesid*</span></span>

<span data-ttu-id="1a75e-110">Определяет контекст сеанса базы данных, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="1a75e-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="1a75e-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1a75e-111">*tableid*</span></span>

<span data-ttu-id="1a75e-112">Определяет таблицу, которая должна быть закрыта.</span><span class="sxs-lookup"><span data-stu-id="1a75e-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="1a75e-113">Задайте для *tableid* значение JET_tableidNil, чтобы освободить память.</span><span class="sxs-lookup"><span data-stu-id="1a75e-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="1a75e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a75e-114">Return Value</span></span>

<span data-ttu-id="1a75e-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="1a75e-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1a75e-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1a75e-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a75e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1a75e-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="1a75e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1a75e-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a75e-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1a75e-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1a75e-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1a75e-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1a75e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a75e-121">Remarks</span></span>

<span data-ttu-id="1a75e-122">Эта функция должна вызываться для всех таблиц, открытых с помощью [жетопентабле](./jetopentable-function.md).</span><span class="sxs-lookup"><span data-stu-id="1a75e-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="1a75e-123">Исключение из этого правила происходит при вызове [жетопентабле](./jetopentable-function.md) в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="1a75e-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="1a75e-124">При откате транзакции таблица автоматически закрывается.</span><span class="sxs-lookup"><span data-stu-id="1a75e-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="1a75e-125">В этом случае возникает ошибка при закрытии таблицы с помощью **жетклосетабле**.</span><span class="sxs-lookup"><span data-stu-id="1a75e-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1a75e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1a75e-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a75e-127"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1a75e-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1a75e-128">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1a75e-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a75e-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1a75e-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1a75e-130">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1a75e-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a75e-131"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1a75e-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1a75e-132">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1a75e-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a75e-133"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="1a75e-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1a75e-134">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1a75e-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a75e-135"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="1a75e-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1a75e-136">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1a75e-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1a75e-137">См. также:</span><span class="sxs-lookup"><span data-stu-id="1a75e-137">See Also</span></span>

[<span data-ttu-id="1a75e-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1a75e-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1a75e-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1a75e-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1a75e-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1a75e-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1a75e-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1a75e-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1a75e-142">жетопентабле</span><span class="sxs-lookup"><span data-stu-id="1a75e-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="1a75e-143">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="1a75e-143">JetRollback</span></span>](./jetrollback-function.md)
