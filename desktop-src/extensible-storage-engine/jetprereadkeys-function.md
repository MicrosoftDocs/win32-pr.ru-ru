---
description: Дополнительные сведения о функции Жетпререадкэйс
title: Функция Жетпререадкэйс
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497409"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="41bdd-103">Функция Жетпререадкэйс</span><span class="sxs-lookup"><span data-stu-id="41bdd-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="41bdd-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="41bdd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="41bdd-105">Функция Жетпререадкэйс</span><span class="sxs-lookup"><span data-stu-id="41bdd-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="41bdd-106">Функция **жетпререадкэйс** считывает значения ключей для повышения производительности очистки хранилища версий.</span><span class="sxs-lookup"><span data-stu-id="41bdd-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="41bdd-107">**Windows 7: функция пререадкэйс** появилась в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41bdd-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="41bdd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41bdd-108">Parameters</span></span>

<span data-ttu-id="41bdd-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="41bdd-109">*sesid*</span></span>

<span data-ttu-id="41bdd-110">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="41bdd-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="41bdd-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="41bdd-111">*tableid*</span></span>

<span data-ttu-id="41bdd-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="41bdd-112">The cursor to use for this call.</span></span>

<span data-ttu-id="41bdd-113">*ргпвкэйс*</span><span class="sxs-lookup"><span data-stu-id="41bdd-113">*rgpvKeys*</span></span>

<span data-ttu-id="41bdd-114">Массив указателей на ключи.</span><span class="sxs-lookup"><span data-stu-id="41bdd-114">An array of pointers to keys.</span></span> <span data-ttu-id="41bdd-115">Ключи можно создавать с помощью [жетмакекэй](./jetmakekey-function.md) или извлекать с помощью [жетжетбукмарк](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="41bdd-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="41bdd-116">Ключи должны быть отсортированы в порядке возрастания или убывания в зависимости от переданного грбит.</span><span class="sxs-lookup"><span data-stu-id="41bdd-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="41bdd-117">Ключи можно сортировать с помощью memcmp.</span><span class="sxs-lookup"><span data-stu-id="41bdd-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="41bdd-118">*ргкбкэйс*</span><span class="sxs-lookup"><span data-stu-id="41bdd-118">*rgcbKeys*</span></span>

<span data-ttu-id="41bdd-119">Массив длин ключей.</span><span class="sxs-lookup"><span data-stu-id="41bdd-119">An array of key lengths.</span></span> <span data-ttu-id="41bdd-120">Ргпвкэйс \[ n \] должен указывать на ключ длины ргкбкэйс \[ n\]</span><span class="sxs-lookup"><span data-stu-id="41bdd-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="41bdd-121">*ккэйс*</span><span class="sxs-lookup"><span data-stu-id="41bdd-121">*ckeys*</span></span>

<span data-ttu-id="41bdd-122">Количество ключей.</span><span class="sxs-lookup"><span data-stu-id="41bdd-122">The number of keys.</span></span> <span data-ttu-id="41bdd-123">Ргпвкэйс и Ргкбкэйс должны указывать на массив по крайней мере ккэйс элементов.</span><span class="sxs-lookup"><span data-stu-id="41bdd-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="41bdd-124">*пккэйспререад*</span><span class="sxs-lookup"><span data-stu-id="41bdd-124">*pckeysPreread*</span></span>

<span data-ttu-id="41bdd-125">Возвращает число ключей, для которых фактически были выданы данные для чтения.</span><span class="sxs-lookup"><span data-stu-id="41bdd-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="41bdd-126">Этот параметр может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="41bdd-126">This parameter can be NULL.</span></span>

<span data-ttu-id="41bdd-127">*грбит*</span><span class="sxs-lookup"><span data-stu-id="41bdd-127">*grbit*</span></span>

<span data-ttu-id="41bdd-128">Это должен быть либо JET_bitPrereadForward, либо JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="41bdd-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="41bdd-129">Если грбит имеет JET_bitPrereadForward, ключи должны быть отсортированы в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="41bdd-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="41bdd-130">Если грбит имеет JET_bitPrereadBackward, ключи должны быть отсортированы в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="41bdd-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="41bdd-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41bdd-131">Return Value</span></span>

<span data-ttu-id="41bdd-132">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="41bdd-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="41bdd-133">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="41bdd-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="41bdd-134">Ошибки ввода-вывода могут возвращаться вместе со следующими ошибками использования API:</span><span class="sxs-lookup"><span data-stu-id="41bdd-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41bdd-135">Код возврата</span><span class="sxs-lookup"><span data-stu-id="41bdd-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="41bdd-136">Описание</span><span class="sxs-lookup"><span data-stu-id="41bdd-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41bdd-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="41bdd-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="41bdd-138">Грбит не был ни JET_bitPrereadForward, ни JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="41bdd-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41bdd-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="41bdd-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="41bdd-140">Передан неверный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="41bdd-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="41bdd-141">Ключи не могут иметь значение 0 и не превышать максимальную длину ключа для таблицы.</span><span class="sxs-lookup"><span data-stu-id="41bdd-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41bdd-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="41bdd-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="41bdd-143">Передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="41bdd-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="41bdd-144">Это может быть вызвано значением NULL для обязательного параметра или может означать, что массив ключей не отсортирован должным образом.</span><span class="sxs-lookup"><span data-stu-id="41bdd-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41bdd-145">**Жетпререадкэйс** проходит внутренние страницы сбалансированного дерева, чтобы определить, какие конечные страницы содержат ключи, указанные в Ргпвкэйс/ргкбкэйс.</span><span class="sxs-lookup"><span data-stu-id="41bdd-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="41bdd-146">Список конечных страниц сортируется, а затем для диапазонов страниц выводятся данные для чтения.</span><span class="sxs-lookup"><span data-stu-id="41bdd-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="41bdd-147">Число страниц, которые могут быть доступны для чтения, ограничено, поэтому возможно, что не все ключи могут быть считаны.</span><span class="sxs-lookup"><span data-stu-id="41bdd-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="41bdd-148">В этом случае число ключей, фактически прочитанных в Пккэйспререад, будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="41bdd-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="41bdd-149">Требования</span><span class="sxs-lookup"><span data-stu-id="41bdd-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41bdd-150"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="41bdd-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="41bdd-151">Требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41bdd-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41bdd-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="41bdd-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="41bdd-153">Требуется Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="41bdd-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41bdd-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="41bdd-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="41bdd-155">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="41bdd-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41bdd-156"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="41bdd-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="41bdd-157">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="41bdd-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41bdd-158"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="41bdd-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="41bdd-159">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="41bdd-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
