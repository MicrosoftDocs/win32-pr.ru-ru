---
description: 'Дополнительные сведения: обработка ошибок параметров'
title: Параметры обработки ошибок
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913352"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="aef8b-103">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="aef8b-103">Error Handling Parameters</span></span>


<span data-ttu-id="aef8b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aef8b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="aef8b-105">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="aef8b-105">Error Handling Parameters</span></span>

<span data-ttu-id="aef8b-106">Этот раздел содержит параметры, используемые для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="aef8b-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="aef8b-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="aef8b-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="aef8b-108">Этот параметр можно использовать для преобразования [JET_ERR](./jet-err.md) в строку.</span><span class="sxs-lookup"><span data-stu-id="aef8b-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="aef8b-109">Это делается с помощью специального вызова [жетжетсистемпараметер](./jetgetsystemparameter-function.md) , где выходной буфер выходных данных содержит [JET_ERR](./jet-err.md) значение для преобразования (в качестве входного параметра), а строковый выходной буфер возвращает соответствующую строку ошибки.</span><span class="sxs-lookup"><span data-stu-id="aef8b-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="aef8b-110">Строка будет выглядеть примерно следующим образом: "JET_errSuccess, успешная операция".</span><span class="sxs-lookup"><span data-stu-id="aef8b-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="aef8b-111">Строка состоит из символьного имени строки, затем запятой, а затем простого текстового описания ошибки.</span><span class="sxs-lookup"><span data-stu-id="aef8b-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="aef8b-112">Строка описания может содержать запятые.</span><span class="sxs-lookup"><span data-stu-id="aef8b-112">The description string may itself contain commas.</span></span> <span data-ttu-id="aef8b-113">Если ошибка не распознана, строка будет иметь значение "Неизвестная ошибка, неизвестная ошибка".</span><span class="sxs-lookup"><span data-stu-id="aef8b-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="aef8b-114">**Примечание**  .  Этот параметр доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="aef8b-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-115">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="aef8b-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-116">Специальные функции</span><span class="sxs-lookup"><span data-stu-id="aef8b-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-117">Тип:</span><span class="sxs-lookup"><span data-stu-id="aef8b-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-118">Специальные функции</span><span class="sxs-lookup"><span data-stu-id="aef8b-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-119">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="aef8b-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-120">Специальные функции</span><span class="sxs-lookup"><span data-stu-id="aef8b-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-121">Область.</span><span class="sxs-lookup"><span data-stu-id="aef8b-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-122">Глобальный</span><span class="sxs-lookup"><span data-stu-id="aef8b-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-123">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="aef8b-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-124">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-125">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="aef8b-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-126">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-127">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="aef8b-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-128">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-129">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="aef8b-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-130">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-131">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="aef8b-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-132">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-133">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="aef8b-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-134">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-135">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="aef8b-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-136">Все</span><span class="sxs-lookup"><span data-stu-id="aef8b-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aef8b-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="aef8b-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="aef8b-138">98</span><span class="sxs-lookup"><span data-stu-id="aef8b-138">98</span></span>  

<span data-ttu-id="aef8b-139">Этот параметр определяет, что происходит при возникновении исключения ядром СУБД или кодом, который вызывается ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="aef8b-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="aef8b-140">Если задано значение JET_ExceptionMsgBox, в фильтр необработанных исключений Windows будет создано любое исключение.</span><span class="sxs-lookup"><span data-stu-id="aef8b-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="aef8b-141">Это приведет к тому, что исключение будет обработано как сбой приложения.</span><span class="sxs-lookup"><span data-stu-id="aef8b-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="aef8b-142">Цель состоит в том, чтобы предотвратить ошибочную попытку перехвата и игнорирования исключения, созданного ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="aef8b-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="aef8b-143">Это не может быть разрешено, так как может произойти повреждение базы данных.</span><span class="sxs-lookup"><span data-stu-id="aef8b-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="aef8b-144">Если приложение должно правильно обрабатывать эти исключения, можно отключить защиту, присвоив этому параметру значение JET_ExceptionNone.</span><span class="sxs-lookup"><span data-stu-id="aef8b-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-145">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="aef8b-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="aef8b-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-147">Тип:</span><span class="sxs-lookup"><span data-stu-id="aef8b-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-148">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="aef8b-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-149">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="aef8b-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-150">JET_ExceptionMsgBox, JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="aef8b-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-151">Область.</span><span class="sxs-lookup"><span data-stu-id="aef8b-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-152">Глобальный</span><span class="sxs-lookup"><span data-stu-id="aef8b-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-153">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="aef8b-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-154">Windows <strong>2000, Windows XP и Windows Server 2003:</strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="aef8b-155"><strong>Windows Vista:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="aef8b-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-156">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="aef8b-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-157">Windows <strong>2000, Windows XP и Windows Server 2003:</strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="aef8b-158"><strong>Windows Vista:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="aef8b-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-159">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="aef8b-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-160">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-161">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="aef8b-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-162">Да</span><span class="sxs-lookup"><span data-stu-id="aef8b-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-163">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="aef8b-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-164">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-165">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="aef8b-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-166">Нет</span><span class="sxs-lookup"><span data-stu-id="aef8b-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-167">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="aef8b-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aef8b-168">Все</span><span class="sxs-lookup"><span data-stu-id="aef8b-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="aef8b-169">Требования</span><span class="sxs-lookup"><span data-stu-id="aef8b-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-170"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="aef8b-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aef8b-171">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="aef8b-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aef8b-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="aef8b-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aef8b-173">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aef8b-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aef8b-174"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="aef8b-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aef8b-175">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="aef8b-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="aef8b-176">См. также:</span><span class="sxs-lookup"><span data-stu-id="aef8b-176">See Also</span></span>

[<span data-ttu-id="aef8b-177">Константы обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="aef8b-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="aef8b-178">Коды ошибок расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="aef8b-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="aef8b-179">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="aef8b-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="aef8b-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aef8b-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aef8b-181">жетинит</span><span class="sxs-lookup"><span data-stu-id="aef8b-181">JetInit</span></span>](./jetinit-function.md)
