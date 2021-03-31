---
description: Дополнительные сведения о функции Жетидле
title: Функция Жетидле
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911439"
---
# <a name="jetidle-function"></a><span data-ttu-id="50626-103">Функция Жетидле</span><span class="sxs-lookup"><span data-stu-id="50626-103">JetIdle Function</span></span>


<span data-ttu-id="50626-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="50626-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="50626-105">Функция Жетидле</span><span class="sxs-lookup"><span data-stu-id="50626-105">JetIdle Function</span></span>

<span data-ttu-id="50626-106">Функция **жетидле** уничтожена, и ее следует использовать только в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="50626-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="50626-107">**Жетидле** можно использовать для выполнения задач очистки после простоя или для проверки состояния хранилища версий в ESE.</span><span class="sxs-lookup"><span data-stu-id="50626-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="50626-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50626-108">Parameters</span></span>

<span data-ttu-id="50626-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="50626-109">*sesid*</span></span>

<span data-ttu-id="50626-110">Сеанс, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="50626-110">The session that will be used for this call.</span></span>

<span data-ttu-id="50626-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="50626-111">*grbit*</span></span>

<span data-ttu-id="50626-112">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих битов:</span><span class="sxs-lookup"><span data-stu-id="50626-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50626-113">Значение</span><span class="sxs-lookup"><span data-stu-id="50626-113">Value</span></span></p></th>
<th><p><span data-ttu-id="50626-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50626-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50626-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="50626-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="50626-116">Запускает очистку хранилища версий.</span><span class="sxs-lookup"><span data-stu-id="50626-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50626-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="50626-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="50626-118">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="50626-118">Reserved for future use.</span></span> <span data-ttu-id="50626-119">Если этот флаг указан, API возвратит JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="50626-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50626-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="50626-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="50626-121">Возвращает JET_wrnIdleFull, если хранилище версий больше половины места.</span><span class="sxs-lookup"><span data-stu-id="50626-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="50626-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50626-122">Return Value</span></span>

<span data-ttu-id="50626-123">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="50626-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="50626-124">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="50626-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50626-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="50626-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="50626-126">Описание</span><span class="sxs-lookup"><span data-stu-id="50626-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50626-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="50626-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="50626-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="50626-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50626-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="50626-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="50626-130">Недопустимый параметр <em>грбит</em> , предоставленный API.</span><span class="sxs-lookup"><span data-stu-id="50626-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50626-131">Если эта функция завершится с ошибкой, будет активирована соответствующая операция или код ошибки, указывающий, насколько заполнено хранилище версий в зависимости от предоставленной *грбит* .</span><span class="sxs-lookup"><span data-stu-id="50626-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="50626-132">Если эта функция завершается ошибкой, запрошенная операция не будет выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="50626-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50626-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50626-133">Remarks</span></span>

<span data-ttu-id="50626-134">Хранилище версий поддерживает механизм изоляции моментальных снимков ESE.</span><span class="sxs-lookup"><span data-stu-id="50626-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="50626-135">Если хранилище версий больше половины, программа может закрыть долго выполняющиеся транзакции.</span><span class="sxs-lookup"><span data-stu-id="50626-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="50626-136">Если долго выполняющаяся транзакция приводит к исчерпанию хранилища версий, ESE прекращает разрешение операций записи в базу данных.</span><span class="sxs-lookup"><span data-stu-id="50626-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="50626-137">Требования</span><span class="sxs-lookup"><span data-stu-id="50626-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50626-138"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="50626-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="50626-139">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="50626-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50626-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="50626-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="50626-141">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="50626-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50626-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="50626-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="50626-143">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="50626-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50626-144"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="50626-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="50626-145">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="50626-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50626-146"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="50626-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="50626-147">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="50626-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="50626-148">См. также:</span><span class="sxs-lookup"><span data-stu-id="50626-148">See Also</span></span>

[<span data-ttu-id="50626-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="50626-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="50626-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="50626-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="50626-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="50626-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="50626-152">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="50626-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
