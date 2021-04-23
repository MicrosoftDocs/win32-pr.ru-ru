---
description: Дополнительные сведения о функции Жеткреатеиндекс
title: Функция JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712072"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="92a5a-103">Функция JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="92a5a-103">JetCreateIndex Function</span></span>


<span data-ttu-id="92a5a-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="92a5a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="92a5a-105">Функция JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="92a5a-105">JetCreateIndex Function</span></span>

<span data-ttu-id="92a5a-106">Функция **жеткреатеиндекс** позволяет создавать индексы данных в базе данных ESE, которая позволяет быстро находить нужные данные.</span><span class="sxs-lookup"><span data-stu-id="92a5a-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="92a5a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="92a5a-107">Parameters</span></span>

<span data-ttu-id="92a5a-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="92a5a-108">*sesid*</span></span>

<span data-ttu-id="92a5a-109">Контекст сеанса базы данных, используемый для конкретного вызова API.</span><span class="sxs-lookup"><span data-stu-id="92a5a-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="92a5a-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="92a5a-110">*tableid*</span></span>

<span data-ttu-id="92a5a-111">Таблица, для которой будет создан индекс.</span><span class="sxs-lookup"><span data-stu-id="92a5a-111">The table that an index will be created for.</span></span>

<span data-ttu-id="92a5a-112">*сзиндекснаме*</span><span class="sxs-lookup"><span data-stu-id="92a5a-112">*szIndexName*</span></span>

<span data-ttu-id="92a5a-113">Указатель на строку, завершающуюся нулем, которая указывает имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="92a5a-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="92a5a-114">Имя индекса должно соответствовать следующим рекомендациям:</span><span class="sxs-lookup"><span data-stu-id="92a5a-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="92a5a-115">Оно должно содержать меньше символов, чем JET_cbNameMost, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="92a5a-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="92a5a-116">Он должен содержать только символы из следующих категорий: от 0 до 9, от A до Z, от a до z и всех знаков препинания, кроме " \! "</span><span class="sxs-lookup"><span data-stu-id="92a5a-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="92a5a-117">(восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.</span><span class="sxs-lookup"><span data-stu-id="92a5a-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="92a5a-118">Оно не должно начинаться с пробела.</span><span class="sxs-lookup"><span data-stu-id="92a5a-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="92a5a-119">Он должен содержать по крайней мере один символ, не являющийся пробелом.</span><span class="sxs-lookup"><span data-stu-id="92a5a-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="92a5a-120">*грбит*</span><span class="sxs-lookup"><span data-stu-id="92a5a-120">*grbit*</span></span>

<span data-ttu-id="92a5a-121">Группа битов, содержащая параметры, используемые для конкретного вызова.</span><span class="sxs-lookup"><span data-stu-id="92a5a-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="92a5a-122">Этот параметр может содержать ноль или более параметров, найденных в структуре [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="92a5a-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="92a5a-123">*сзкэй*</span><span class="sxs-lookup"><span data-stu-id="92a5a-123">*szKey*</span></span>

<span data-ttu-id="92a5a-124">Указатель на строку, завершающуюся двойной нулем и заканчивающуюся токеном с разделителями null.</span><span class="sxs-lookup"><span data-stu-id="92a5a-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="92a5a-125">Дополнительные сведения об этом параметре см. в разделе Структура [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="92a5a-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="92a5a-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="92a5a-126">*cbKey*</span></span>

<span data-ttu-id="92a5a-127">Длина (в байтах) параметра *сзкэй* , включая два завершающих нуль символа.</span><span class="sxs-lookup"><span data-stu-id="92a5a-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="92a5a-128">*лденсити*</span><span class="sxs-lookup"><span data-stu-id="92a5a-128">*lDensity*</span></span>

<span data-ttu-id="92a5a-129">Процентная плотность начального дерева B +.</span><span class="sxs-lookup"><span data-stu-id="92a5a-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="92a5a-130">Дополнительные сведения об этом параметре см. в разделе Структура [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="92a5a-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="92a5a-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92a5a-131">Return Value</span></span>

<span data-ttu-id="92a5a-132">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="92a5a-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="92a5a-133">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="92a5a-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92a5a-134">Код возврата</span><span class="sxs-lookup"><span data-stu-id="92a5a-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="92a5a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="92a5a-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92a5a-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="92a5a-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="92a5a-137">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="92a5a-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92a5a-138">Список дополнительных ошибок, которые могут возвращаться функцией **жеткреатеиндекс** , см. в разделе [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="92a5a-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="92a5a-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92a5a-139">Remarks</span></span>

<span data-ttu-id="92a5a-140">Вызов функции **жеткреатеиндекс** идентичен вызову функции [JetCreateIndex2](./jetcreateindex2-function.md) с структурой [JET_INDEXCREATE](./jet-indexcreate-structure.md) , содержащей те же параметры, что и параметры **жеткреатеиндекс**, и параметр *Циндекскреате* , равный 1.</span><span class="sxs-lookup"><span data-stu-id="92a5a-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="92a5a-141">Для полей структуры [JET_INDEXCREATE](./jet-indexcreate-structure.md) , которые не имеют соответствующих параметров в **жеткреатеиндекс**, предполагается значение 0.</span><span class="sxs-lookup"><span data-stu-id="92a5a-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="92a5a-142">Обратите внимание, что **жеткреатеиндекс** был заменен [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="92a5a-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="92a5a-143">Требования</span><span class="sxs-lookup"><span data-stu-id="92a5a-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92a5a-144">Клиент</span><span class="sxs-lookup"><span data-stu-id="92a5a-144">Client</span></span></p></td>
<td><p><span data-ttu-id="92a5a-145">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="92a5a-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92a5a-146">Сервер</span><span class="sxs-lookup"><span data-stu-id="92a5a-146">Server</span></span></p></td>
<td><p><span data-ttu-id="92a5a-147">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="92a5a-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92a5a-148">Header</span><span class="sxs-lookup"><span data-stu-id="92a5a-148">Header</span></span></p></td>
<td><p><span data-ttu-id="92a5a-149">Объявляется в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="92a5a-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92a5a-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92a5a-150">Library</span></span></p></td>
<td><p><span data-ttu-id="92a5a-151">Использует ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="92a5a-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92a5a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="92a5a-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="92a5a-153">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="92a5a-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92a5a-154">Юникод</span><span class="sxs-lookup"><span data-stu-id="92a5a-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="92a5a-155">Реализуется как <strong>жеткреатеиндексв</strong> (Юникод) и <strong>жеткреатеиндекса</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="92a5a-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="92a5a-156">См. также:</span><span class="sxs-lookup"><span data-stu-id="92a5a-156">See Also</span></span>

[<span data-ttu-id="92a5a-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="92a5a-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="92a5a-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="92a5a-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="92a5a-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="92a5a-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="92a5a-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="92a5a-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="92a5a-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="92a5a-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="92a5a-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="92a5a-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="92a5a-163">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="92a5a-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="92a5a-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="92a5a-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
