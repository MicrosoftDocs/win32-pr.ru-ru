---
description: Дополнительные сведения о функции Жетжетобжектинфо
title: Функция JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712070"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="52c69-103">Функция JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="52c69-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="52c69-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52c69-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="52c69-105">Функция JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="52c69-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="52c69-106">Функция **жетжетобжектинфо** извлекает сведения об объектах базы данных.</span><span class="sxs-lookup"><span data-stu-id="52c69-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="52c69-107">В настоящее время поддерживаются только таблицы.</span><span class="sxs-lookup"><span data-stu-id="52c69-107">Currently, only tables are supported.</span></span> <span data-ttu-id="52c69-108">[Жетжеттаблеинфо](./jetgettableinfo-function.md) можно использовать для получения дополнительных сведений, чем **жетжетобжектинфо**.</span><span class="sxs-lookup"><span data-stu-id="52c69-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="52c69-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="52c69-109">Parameters</span></span>

<span data-ttu-id="52c69-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="52c69-110">*sesid*</span></span>

<span data-ttu-id="52c69-111">Используемый контекст сеанса базы данных.</span><span class="sxs-lookup"><span data-stu-id="52c69-111">The database session context to use.</span></span>

<span data-ttu-id="52c69-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="52c69-112">*dbid*</span></span>

<span data-ttu-id="52c69-113">База данных, из которой извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="52c69-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="52c69-114">*обжтип*</span><span class="sxs-lookup"><span data-stu-id="52c69-114">*objtyp*</span></span>

<span data-ttu-id="52c69-115">Объекты, содержащие сведения для извлечения.</span><span class="sxs-lookup"><span data-stu-id="52c69-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="52c69-116">В настоящее время поддерживаются только JET_objtypNil и JET_objtypTable, которые ведут себя одинаково.</span><span class="sxs-lookup"><span data-stu-id="52c69-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="52c69-117">Будут получены только таблицы.</span><span class="sxs-lookup"><span data-stu-id="52c69-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="52c69-118">*сзконтаинернаме*</span><span class="sxs-lookup"><span data-stu-id="52c69-118">*szContainerName*</span></span>

<span data-ttu-id="52c69-119">Этот параметр зарезервирован для будущего использования и передает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="52c69-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="52c69-120">Имена типов объектов, сведения о которых необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="52c69-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="52c69-121">*сзобжектнаме*</span><span class="sxs-lookup"><span data-stu-id="52c69-121">*szObjectName*</span></span>

<span data-ttu-id="52c69-122">Имя объекта, который содержит извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="52c69-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="52c69-123">Если *инфолевел* использует параметры JET_ObjInfoList или JET_ObjInfoListNoStats для получения списка всех объектов, это значение должно быть **равно NULL** или быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="52c69-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="52c69-124">В настоящее время поддерживаются только имена таблиц.</span><span class="sxs-lookup"><span data-stu-id="52c69-124">Only table names are currently supported.</span></span>

<span data-ttu-id="52c69-125">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="52c69-125">*pvResult*</span></span>

<span data-ttu-id="52c69-126">Указатель на буфер, который получает указанные сведения.</span><span class="sxs-lookup"><span data-stu-id="52c69-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="52c69-127">Размер буфера в байтах передается в *кбмакс*.</span><span class="sxs-lookup"><span data-stu-id="52c69-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="52c69-128">При сбое содержимое *пвресулт* не определено.</span><span class="sxs-lookup"><span data-stu-id="52c69-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="52c69-129">Сведения, хранящиеся в *пвресулт* , зависят от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="52c69-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="52c69-130">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="52c69-130">*cbMax*</span></span>

<span data-ttu-id="52c69-131">Размер буфера (в байтах), переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="52c69-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="52c69-132">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="52c69-132">*InfoLevel*</span></span>

<span data-ttu-id="52c69-133">Указывает, какой тип данных получить для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="52c69-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="52c69-134">Это влияет на интерпретацию *пвресулт* .</span><span class="sxs-lookup"><span data-stu-id="52c69-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="52c69-135">Для этого параметра можно задать следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="52c69-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52c69-136">Значение</span><span class="sxs-lookup"><span data-stu-id="52c69-136">Value</span></span></p></th>
<th><p><span data-ttu-id="52c69-137">Значение</span><span class="sxs-lookup"><span data-stu-id="52c69-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52c69-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="52c69-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="52c69-139"><em>пвресулт</em> интерпретируется как структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="52c69-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="52c69-140">Структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> заполняется сведениями, относящимися к объекту с именем в <em>сзобжектнаме</em>.</span><span class="sxs-lookup"><span data-stu-id="52c69-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="52c69-141">Если вызывающему объекту не требуется знание количества записей и страниц для объекта, рекомендуется использовать JET_ObjInfoNoStats уровень информации, который может быть быстрее, так как статистика не включена.</span><span class="sxs-lookup"><span data-stu-id="52c69-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="52c69-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="52c69-143"><em>пвресулт</em> интерпретируется как структура <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="52c69-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="52c69-144">Извлекаются сведения обо всех объектах.</span><span class="sxs-lookup"><span data-stu-id="52c69-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="52c69-145">Будет создана временная таблица, а сведения, необходимые для обхода временной таблицы, описаны в структуре <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="52c69-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="52c69-146">Дополнительные сведения см. в разделе <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="52c69-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="52c69-147">Если вызывающему объекту не требуется знание количества записей и страниц для объекта, рассмотрите возможность использования JET_ObjInfoListNoStats, что может быть быстрее.</span><span class="sxs-lookup"><span data-stu-id="52c69-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="52c69-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="52c69-149">Не рекомендуется и не поддерживается в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="52c69-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="52c69-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="52c69-151"><em>пвресулт</em> интерпретируется как структура <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="52c69-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="52c69-152">Извлекаются сведения обо всех объектах.</span><span class="sxs-lookup"><span data-stu-id="52c69-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="52c69-153">Будет создана временная таблица, а сведения, необходимые для обхода временной таблицы, описаны в структуре <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="52c69-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="52c69-154">Дополнительные сведения см. в разделе <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="52c69-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="52c69-155">JET_ObjInfoListNoStats идентично JET_ObjInfoList, за исключением того, что столбцы, сообщающие о количестве записей (<em>колумнидкрекорд</em>) и страницах (<em>колумнидкпаже</em>), не обновляются.</span><span class="sxs-lookup"><span data-stu-id="52c69-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="52c69-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="52c69-157"><em>пвресулт</em> интерпретируется как <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="52c69-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="52c69-158">Максимальный размер объекта находится на страницах.</span><span class="sxs-lookup"><span data-stu-id="52c69-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="52c69-159">В настоящее время возвращаются только таблицы.</span><span class="sxs-lookup"><span data-stu-id="52c69-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="52c69-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="52c69-161"><em>пвресулт</em> интерпретируется как <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="52c69-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="52c69-162">Будут получены сведения только о объекте, указанном в <em>сзобжектнаме</em> .</span><span class="sxs-lookup"><span data-stu-id="52c69-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="52c69-163">Структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> будет заполнена сведениями, относящимися к объекту с именем в <em>сзобжектнаме</em>.</span><span class="sxs-lookup"><span data-stu-id="52c69-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="52c69-164">JET_ObjInfoNoStats идентично JET_ObjInfo, за исключением того, что поля, сообщающие число записей и страниц, имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="52c69-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="52c69-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="52c69-166">Не рекомендуется и не поддерживается в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="52c69-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="52c69-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="52c69-168">Не рекомендуется и не поддерживается в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="52c69-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="52c69-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="52c69-170">Не рекомендуется и не поддерживается в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="52c69-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="52c69-171">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52c69-171">Return Value</span></span>

<span data-ttu-id="52c69-172">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="52c69-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="52c69-173">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="52c69-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52c69-174">Код возврата</span><span class="sxs-lookup"><span data-stu-id="52c69-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="52c69-175">Описание</span><span class="sxs-lookup"><span data-stu-id="52c69-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52c69-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="52c69-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="52c69-177">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="52c69-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="52c69-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="52c69-179">Размер буфера, заданного в <em>кбмакс</em> , слишком мал для хранения требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="52c69-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="52c69-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="52c69-181">В <em>сзобжектнаме</em> или <em>сзконтаинернаме</em>было указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="52c69-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="52c69-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="52c69-183">Передан неверный параметр.</span><span class="sxs-lookup"><span data-stu-id="52c69-183">A bad parameter was given.</span></span> <span data-ttu-id="52c69-184">Возможно, в <em>инфолевел</em>был передан недопустимый уровень.</span><span class="sxs-lookup"><span data-stu-id="52c69-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="52c69-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52c69-185">Remarks</span></span>

<span data-ttu-id="52c69-186">Если **жетжетобжектинфо** успешно создает временную таблицу (например, JET_ObjInfoList или JET_ObjInfoNoStats), вызывающий объект отвечает за закрытие временной таблицы с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="52c69-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="52c69-187">В настоящее время **жетжетобжектинфо** поддерживает только получение сведений о таблицах.</span><span class="sxs-lookup"><span data-stu-id="52c69-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="52c69-188">Требования</span><span class="sxs-lookup"><span data-stu-id="52c69-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52c69-189"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="52c69-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="52c69-190">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="52c69-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="52c69-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="52c69-192">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="52c69-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="52c69-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="52c69-194">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="52c69-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-195"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="52c69-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="52c69-196">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="52c69-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52c69-197"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="52c69-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="52c69-198">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="52c69-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52c69-199"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="52c69-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="52c69-200">Реализуется как <strong>жетжетобжектинфов</strong> (Юникод) и <strong>жетжетобжектинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="52c69-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="52c69-201">См. также:</span><span class="sxs-lookup"><span data-stu-id="52c69-201">See Also</span></span>

[<span data-ttu-id="52c69-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="52c69-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="52c69-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="52c69-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="52c69-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="52c69-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="52c69-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="52c69-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="52c69-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="52c69-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="52c69-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="52c69-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="52c69-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="52c69-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="52c69-209">жетклосетабле</span><span class="sxs-lookup"><span data-stu-id="52c69-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="52c69-210">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="52c69-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
