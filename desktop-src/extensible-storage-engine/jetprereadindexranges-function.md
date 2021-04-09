---
description: Дополнительные сведения о функции Жетпререадиндексранжес
title: Функция Жетпререадиндексранжес
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143522"
---
# <a name="jetprereadindexranges-function"></a><span data-ttu-id="4ee54-103">Функция Жетпререадиндексранжес</span><span class="sxs-lookup"><span data-stu-id="4ee54-103">JetPrereadIndexRanges Function</span></span>


<span data-ttu-id="4ee54-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4ee54-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="4ee54-105">Функция **жетпререадиндексранжес** считывает индексы для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="4ee54-105">The **JetPrereadIndexRanges** function prereads indexes to improve the performance.</span></span>

<span data-ttu-id="4ee54-106">Функция **жетпререадиндексранжес** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ee54-106">The **JetPrereadIndexRanges** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="4ee54-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ee54-107">Parameters</span></span>

<span data-ttu-id="4ee54-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="4ee54-108">*sesid*</span></span>

<span data-ttu-id="4ee54-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="4ee54-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="4ee54-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4ee54-110">*tableid*</span></span>

<span data-ttu-id="4ee54-111">Таблица, для которой выдаются сведения о предчтении.</span><span class="sxs-lookup"><span data-stu-id="4ee54-111">The table to issue the prereads against.</span></span>

<span data-ttu-id="4ee54-112">*ргиндексранжес*</span><span class="sxs-lookup"><span data-stu-id="4ee54-112">*rgIndexRanges*</span></span>

<span data-ttu-id="4ee54-113">Диапазоны ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="4ee54-113">The key ranges to preread.</span></span>

<span data-ttu-id="4ee54-114">*Циндексранжес*</span><span class="sxs-lookup"><span data-stu-id="4ee54-114">*cIndexRanges*</span></span>

<span data-ttu-id="4ee54-115">Число диапазонов ключей для предчтения, определяемое числом элементов в *ргиндексранжес*.</span><span class="sxs-lookup"><span data-stu-id="4ee54-115">The number of key ranges to preread, determined by the number of elements in *rgIndexRanges*.</span></span>

<span data-ttu-id="4ee54-116">*пкранжеспререад*</span><span class="sxs-lookup"><span data-stu-id="4ee54-116">*pcRangesPreread*</span></span>

<span data-ttu-id="4ee54-117">Количество диапазонов ключей, которые фактически были считаны.</span><span class="sxs-lookup"><span data-stu-id="4ee54-117">The number of key ranges that were actually preread.</span></span>

<span data-ttu-id="4ee54-118">*ргколумнидпререад*</span><span class="sxs-lookup"><span data-stu-id="4ee54-118">*rgcolumnidPreread*</span></span>

<span data-ttu-id="4ee54-119">Список идентификаторов столбцов для столбцов с длинными значениями для чтения.</span><span class="sxs-lookup"><span data-stu-id="4ee54-119">List of column IDs for long value columns to preread.</span></span> <span data-ttu-id="4ee54-120">По умолчанию предварительно считывается только запись на странице.</span><span class="sxs-lookup"><span data-stu-id="4ee54-120">By default, only the on-page record is preread.</span></span> <span data-ttu-id="4ee54-121">Если необходимо предварительно прочитать столбцы с длинными значениями в виде страниц, их идентификаторы столбцов должны передаваться через этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ee54-121">If Off-page long value columns need to be preread, their column IDs need to be passed via this parameter.</span></span>

<span data-ttu-id="4ee54-122">*кколумнидпререад*</span><span class="sxs-lookup"><span data-stu-id="4ee54-122">*ccolumnidPreread*</span></span>

<span data-ttu-id="4ee54-123">Количество идентификаторов столбцов для столбцов с длинными значениями, которые должны быть считаны, определяется числом элементов в *ргколумнидпререад*.</span><span class="sxs-lookup"><span data-stu-id="4ee54-123">The number of column IDs for long value columns to preread, determined by the number of elements in *rgcolumnidPreread*.</span></span>

<span data-ttu-id="4ee54-124">*грбит*</span><span class="sxs-lookup"><span data-stu-id="4ee54-124">*grbit*</span></span>

<span data-ttu-id="4ee54-125">Группа битов, указывающая ноль или более значений направления, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4ee54-125">A group of bits that specifies zero or more of the preread direction values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ee54-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4ee54-126">Value</span></span></p></th>
<th><p><span data-ttu-id="4ee54-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4ee54-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ee54-128">Вперед</span><span class="sxs-lookup"><span data-stu-id="4ee54-128">Forward</span></span></p></td>
<td><p><span data-ttu-id="4ee54-129">Чтение вперед.</span><span class="sxs-lookup"><span data-stu-id="4ee54-129">Preread forward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ee54-130">Назад</span><span class="sxs-lookup"><span data-stu-id="4ee54-130">Backwards</span></span></p></td>
<td><p><span data-ttu-id="4ee54-131">Прочтите обратно.</span><span class="sxs-lookup"><span data-stu-id="4ee54-131">Preread backward.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ee54-132">фирстпажеонли</span><span class="sxs-lookup"><span data-stu-id="4ee54-132">FirstPageOnly</span></span></p></td>
<td><p><span data-ttu-id="4ee54-133">Предварительное чтение только первой страницы любого столбца Long.</span><span class="sxs-lookup"><span data-stu-id="4ee54-133">Preread only the first page of any long column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ee54-134">нормализедкэй</span><span class="sxs-lookup"><span data-stu-id="4ee54-134">NormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="4ee54-135">Нормализованное значение ключа или закладки вместо значения столбца.</span><span class="sxs-lookup"><span data-stu-id="4ee54-135">Normalized key/bookmark provided instead of column value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4ee54-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ee54-136">Return value</span></span>

<span data-ttu-id="4ee54-137">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4ee54-137">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="4ee54-138">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4ee54-138">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ee54-139">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4ee54-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="4ee54-140">Описание</span><span class="sxs-lookup"><span data-stu-id="4ee54-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ee54-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4ee54-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4ee54-142">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4ee54-142">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="4ee54-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ee54-143">Remarks</span></span>

<span data-ttu-id="4ee54-144">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, следует запустить асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="4ee54-144">If the records with the specified key ranges are not in the buffer cache, you should start asynchronous reads to bring the records into the database buffer cache.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4ee54-145">Требования</span><span class="sxs-lookup"><span data-stu-id="4ee54-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ee54-146"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4ee54-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4ee54-147">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ee54-147">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ee54-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4ee54-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4ee54-149">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="4ee54-149">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ee54-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4ee54-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4ee54-151">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4ee54-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ee54-152"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="4ee54-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4ee54-153">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4ee54-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ee54-154"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="4ee54-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4ee54-155">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4ee54-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4ee54-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ee54-156">See also</span></span>

[<span data-ttu-id="4ee54-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4ee54-157">JET_ERR</span></span>](./jet-err.md)
