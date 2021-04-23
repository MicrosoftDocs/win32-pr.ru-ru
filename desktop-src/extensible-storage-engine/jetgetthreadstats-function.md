---
description: Дополнительные сведения о функции Жетжетсреадстатс
title: Функция Жетжетсреадстатс
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701357"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="497f7-103">Функция Жетжетсреадстатс</span><span class="sxs-lookup"><span data-stu-id="497f7-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="497f7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="497f7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="497f7-105">Функция Жетжетсреадстатс</span><span class="sxs-lookup"><span data-stu-id="497f7-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="497f7-106">Функция **жетжетсреадстатс** извлекает сведения о производительности из ядра СУБД для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="497f7-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="497f7-107">Для сбора статистики, отражающей активность ядра СУБД в этом потоке между этими вызовами, можно использовать несколько вызовов.</span><span class="sxs-lookup"><span data-stu-id="497f7-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="497f7-108">**Windows Vista:**  **Жетжетсреадстатс** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="497f7-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="497f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="497f7-109">Parameters</span></span>

<span data-ttu-id="497f7-110">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="497f7-110">*pvResult*</span></span>

<span data-ttu-id="497f7-111">Выходной буфер, который получает данные статистики потока.</span><span class="sxs-lookup"><span data-stu-id="497f7-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="497f7-112">После успешного вызова буфер содержит структуру [JET_THREADSTATS](./jet-threadstats-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="497f7-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="497f7-113">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="497f7-113">*cbMax*</span></span>

<span data-ttu-id="497f7-114">Максимальный размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="497f7-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="497f7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="497f7-115">Return Value</span></span>

<span data-ttu-id="497f7-116">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="497f7-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="497f7-117">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="497f7-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="497f7-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="497f7-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="497f7-119">Описание</span><span class="sxs-lookup"><span data-stu-id="497f7-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="497f7-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="497f7-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="497f7-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="497f7-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="497f7-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="497f7-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="497f7-123">Не удалось выполнить операцию, так как указанный выходной буфер слишком мал для размещения запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="497f7-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="497f7-124">Функция <strong>жетжетсреадстатс</strong> возвращает эту ошибку, если выходной буфер слишком мал для хранения наименьшей версии структуры <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> , поддерживаемой ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="497f7-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="497f7-125">При успешном выполнении выходной буфер будет содержать структуру [JET_THREADSTATS](./jet-threadstats-structure.md) , содержащую статистику ядра СУБД для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="497f7-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="497f7-126">В случае сбоя состояние выходного буфера не определено.</span><span class="sxs-lookup"><span data-stu-id="497f7-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="497f7-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="497f7-127">Remarks</span></span>

<span data-ttu-id="497f7-128">Сведения, предоставляемые двумя последовательными вызовами этого API, предназначены для расчета расходов на любые другие операции ядра СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="497f7-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="497f7-129">Как правило, это делается до и после считывания статистики и вычитания из счетчика Before, чтобы получить общее количество выполненных операций.</span><span class="sxs-lookup"><span data-stu-id="497f7-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="497f7-130">Например, приложение может вызвать **жетжетсреадстатс** один раз, чтобы получить начальное считывание статистики для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="497f7-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="497f7-131">Затем можно вызвать функцию [жетмове](./jetmove-function.md) с параметром *CRowset* , имеющим значение JET_MoveNext, чтобы перейти к следующей записи индекса в индексе.</span><span class="sxs-lookup"><span data-stu-id="497f7-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="497f7-132">Затем можно вызвать **жетжетсреадстатс** еще раз, чтобы получить еще одно считывание статистики потока.</span><span class="sxs-lookup"><span data-stu-id="497f7-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="497f7-133">Затем можно вычесть счетчик Кпажереференцед из второго считывания из первого.</span><span class="sxs-lookup"><span data-stu-id="497f7-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="497f7-134">Результатом будет число страниц базы данных, на которые ссылается ядро СУБД для выполнения операции [жетмове](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="497f7-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="497f7-135">Статистика для каждого потока накапливается в течение времени существования этого потока.</span><span class="sxs-lookup"><span data-stu-id="497f7-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="497f7-136">Статистика сбрасывается, если библиотека DLL ядра СУБД выгружается из хост-процесса.</span><span class="sxs-lookup"><span data-stu-id="497f7-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="497f7-137">Структура [JET_THREADSTATS](./jet-threadstats-structure.md) , скорее всего, будет расширена в будущем, чтобы она содержала больше статистики.</span><span class="sxs-lookup"><span data-stu-id="497f7-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="497f7-138">Новая статистика будет добавлена в конец структуры и может быть извлечена с увеличением размера выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="497f7-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="497f7-139">Наличие дополнительной статистики может быть выведено с помощью большего значения Кбструкт.</span><span class="sxs-lookup"><span data-stu-id="497f7-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="497f7-140">Требования</span><span class="sxs-lookup"><span data-stu-id="497f7-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="497f7-141"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="497f7-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="497f7-142">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="497f7-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="497f7-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="497f7-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="497f7-144">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="497f7-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="497f7-145"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="497f7-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="497f7-146">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="497f7-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="497f7-147"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="497f7-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="497f7-148">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="497f7-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="497f7-149"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="497f7-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="497f7-150">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="497f7-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="497f7-151">См. также:</span><span class="sxs-lookup"><span data-stu-id="497f7-151">See Also</span></span>

[<span data-ttu-id="497f7-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="497f7-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="497f7-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="497f7-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="497f7-154">жетмове</span><span class="sxs-lookup"><span data-stu-id="497f7-154">JetMove</span></span>](./jetmove-function.md)
