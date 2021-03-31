---
description: 'Дополнительные сведения: перечисление JET_ERRCAT'
title: Перечисление JET_ERRCAT (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264787"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="42a48-103">Перечисление JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="42a48-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="42a48-104">Категория ошибки.</span><span class="sxs-lookup"><span data-stu-id="42a48-104">The error category.</span></span> <span data-ttu-id="42a48-105">Иерархия выглядит следующим образом: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//неправильные проблемы ввода-вывода могут быть невременными.</span><span class="sxs-lookup"><span data-stu-id="42a48-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="42a48-106">| |--JET_errcatResource | |--JET_errcatMemory//недостаточно памяти (все варианты) | |--JET_errcatQuota | |--JET_errcatDisk//недостаточно места на диске (все варианты) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//обычно вызвано неисправностью пользователя | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="42a48-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="42a48-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42a48-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="42a48-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42a48-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42a48-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42a48-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="42a48-110">Члены</span><span class="sxs-lookup"><span data-stu-id="42a48-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="42a48-111">Имя участника</span><span class="sxs-lookup"><span data-stu-id="42a48-111">Member name</span></span></th>
<th><span data-ttu-id="42a48-112">Описание</span><span class="sxs-lookup"><span data-stu-id="42a48-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-113">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="42a48-113">Unknown</span></span></td>
<td><span data-ttu-id="42a48-114">Неизвестная Категория.</span><span class="sxs-lookup"><span data-stu-id="42a48-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-115">Ошибка</span><span class="sxs-lookup"><span data-stu-id="42a48-115">Error</span></span></td>
<td><span data-ttu-id="42a48-116">Универсальная Категория.</span><span class="sxs-lookup"><span data-stu-id="42a48-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-117">Операция</span><span class="sxs-lookup"><span data-stu-id="42a48-117">Operation</span></span></td>
<td><span data-ttu-id="42a48-118">Ошибки, которые обычно происходят в любое время из-за неконтролируемых условий.</span><span class="sxs-lookup"><span data-stu-id="42a48-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="42a48-119">Часто временные, но не всегда.</span><span class="sxs-lookup"><span data-stu-id="42a48-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="42a48-120">Восстановление. возможно, повторная попытка или последующее уведомление оператора.</span><span class="sxs-lookup"><span data-stu-id="42a48-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-121">Аварий</span><span class="sxs-lookup"><span data-stu-id="42a48-121">Fatal</span></span></td>
<td><span data-ttu-id="42a48-122">Эта ошибка сортировки возникает только в том случае, если в ESE обнаруживается ошибка, поэтому мы не можем продолжать работу в защищенном (часто транзакционном) способе, а не в поврежденных данных, которые вызовут ошибки этой категории.</span><span class="sxs-lookup"><span data-stu-id="42a48-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="42a48-123">Восстановление. Перезапустите экземпляр или процесс.</span><span class="sxs-lookup"><span data-stu-id="42a48-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="42a48-124">Если проблема сохраняется, сообщите оператору.</span><span class="sxs-lookup"><span data-stu-id="42a48-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-125">IO</span><span class="sxs-lookup"><span data-stu-id="42a48-125">IO</span></span></td>
<td><span data-ttu-id="42a48-126">Ошибки O поступают из операционной системы и выходят за пределы элемента управления ESE. Такая ошибка может быть временной, возможно, невозможной.</span><span class="sxs-lookup"><span data-stu-id="42a48-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="42a48-127">Восстановление. Повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="42a48-127">Recovery: Retry.</span></span> <span data-ttu-id="42a48-128">Если это не разрешено, обратитесь к оператору о проблемах с диском.</span><span class="sxs-lookup"><span data-stu-id="42a48-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-129">Ресурс</span><span class="sxs-lookup"><span data-stu-id="42a48-129">Resource</span></span></td>
<td><span data-ttu-id="42a48-130">Это категория, которая указывает на одно из многих потенциальных условий нехватки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42a48-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-131">Память</span><span class="sxs-lookup"><span data-stu-id="42a48-131">Memory</span></span></td>
<td><span data-ttu-id="42a48-132">Состояние классической нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="42a48-132">Classic out of memory condition.</span></span> <span data-ttu-id="42a48-133">Восстановление: Подождите некоторое время и повторите попытку, освободите память или закройте окно.</span><span class="sxs-lookup"><span data-stu-id="42a48-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-134">Quota</span><span class="sxs-lookup"><span data-stu-id="42a48-134">Quota</span></span></td>
<td><span data-ttu-id="42a48-135">Некоторые &quot; специализированные &quot; ресурсы находятся в пулах определенного размера, что упрощает обнаружение утечек этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42a48-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="42a48-136">Восстановление. может потребоваться внести небольшие изменения в код.</span><span class="sxs-lookup"><span data-stu-id="42a48-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="42a48-137">Для обнаружения этих условий в процессе разработки приложение должно иметь только отладочное действие, например утверждение.</span><span class="sxs-lookup"><span data-stu-id="42a48-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="42a48-138">Для розничного кода рекомендуется рассматривать эту ошибку как ошибку категории памяти и либо повторить попытку, либо освободить память, либо завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="42a48-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-139">Диск</span><span class="sxs-lookup"><span data-stu-id="42a48-139">Disk</span></span></td>
<td><span data-ttu-id="42a48-140">Недостаточно дисковых условий.</span><span class="sxs-lookup"><span data-stu-id="42a48-140">Out of disk conditions.</span></span> <span data-ttu-id="42a48-141">Восстановление. может повторить попытку позже в случае, если освободится больше места, или попросите оператора освободить место на диске.</span><span class="sxs-lookup"><span data-stu-id="42a48-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-142">Данные</span><span class="sxs-lookup"><span data-stu-id="42a48-142">Data</span></span></td>
<td><span data-ttu-id="42a48-143">Ошибка, связанная с данными.</span><span class="sxs-lookup"><span data-stu-id="42a48-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-144">Искажен</span><span class="sxs-lookup"><span data-stu-id="42a48-144">Corruption</span></span></td>
<td><span data-ttu-id="42a48-145">Мой жесткий диск ATE мое домашнее задание.</span><span class="sxs-lookup"><span data-stu-id="42a48-145">My hard drive ate my homework.</span></span> <span data-ttu-id="42a48-146">Проблемы с классическим повреждением, часто постоянные без корректирующих действий.</span><span class="sxs-lookup"><span data-stu-id="42a48-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="42a48-147">Восстановление: восстановление из резервной копии, возможно, операция исправления служебной программы ESE (с сохранением только тех данных, которые остались или теряются). Кроме того, в случае восстановления (Жетинит), возможно, можно выполнить восстановление, добавив возможность потери данных.</span><span class="sxs-lookup"><span data-stu-id="42a48-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-148">Несогласованные</span><span class="sxs-lookup"><span data-stu-id="42a48-148">Inconsistent</span></span></td>
<td><span data-ttu-id="42a48-149">Это похоже на повреждение в том, что база данных и (или) файлы журнала находятся в несогласованном состоянии и не могут быть выверены друг с другом.</span><span class="sxs-lookup"><span data-stu-id="42a48-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="42a48-150">Часто это вызвано неисправностью приложения или администратора.</span><span class="sxs-lookup"><span data-stu-id="42a48-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="42a48-151">Восстановление: восстановление из резервной копии, возможно, операция исправления служебной программы ESE (с сохранением только тех данных, которые остались или теряются).</span><span class="sxs-lookup"><span data-stu-id="42a48-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="42a48-152">Кроме того, в случае восстановления (Жетинит), возможно, можно выполнить восстановление, добавив возможность потери данных.</span><span class="sxs-lookup"><span data-stu-id="42a48-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-153">Фрагментации</span><span class="sxs-lookup"><span data-stu-id="42a48-153">Fragmentation</span></span></td>
<td><span data-ttu-id="42a48-154">Это класс ошибок, в котором был запущен некоторый сохраненный внутренний ресурс. Восстановление. для ошибок базы данных автономная дефрагментация устранит проблему, для файлов журнала _сначала_ восстановите все подключенные базы данных до чистого завершения работы, а затем удалите все файлы журналов и контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="42a48-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-155">API</span><span class="sxs-lookup"><span data-stu-id="42a48-155">Api</span></span></td>
<td><span data-ttu-id="42a48-156">Контейнер для использования и состояния.</span><span class="sxs-lookup"><span data-stu-id="42a48-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-157">Использование</span><span class="sxs-lookup"><span data-stu-id="42a48-157">Usage</span></span></td>
<td><span data-ttu-id="42a48-158">Классическая ошибка использования. Это означает, что код клиента не передает правильные аргументы в API JET.</span><span class="sxs-lookup"><span data-stu-id="42a48-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="42a48-159">Вероятно, эта ошибка не исчезнет с повторным выполнением.</span><span class="sxs-lookup"><span data-stu-id="42a48-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="42a48-160">Восстановление. как правило, код клиента должен утверждать () Этот класс ошибок не возвращается, поэтому проблемы могут быть перехвачены во время разработки.</span><span class="sxs-lookup"><span data-stu-id="42a48-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="42a48-161">В розничной торговле приложение, скорее всего, будет иметь немало вариантов, но не сможет возвращать ошибку оператору.</span><span class="sxs-lookup"><span data-stu-id="42a48-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-162">Состояние</span><span class="sxs-lookup"><span data-stu-id="42a48-162">State</span></span></td>
<td><span data-ttu-id="42a48-163">Это классификация различных сигналов, которые API может возвращать для описания состояния базы данных, классический случай — JET_errRecordNotFound, который может возвращаться Жетсик (), если запрошенная запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="42a48-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="42a48-164">Восстановление: не очень важно, сильно зависит от API.</span><span class="sxs-lookup"><span data-stu-id="42a48-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42a48-165">Устаревшие.</span><span class="sxs-lookup"><span data-stu-id="42a48-165">Obsolete</span></span></td>
<td><span data-ttu-id="42a48-166">Ошибка распознана как допустимая ошибка, но она не должна возвращаться этой версией API.</span><span class="sxs-lookup"><span data-stu-id="42a48-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42a48-167">Макс.</span><span class="sxs-lookup"><span data-stu-id="42a48-167">Max</span></span></td>
<td><span data-ttu-id="42a48-168">Максимальное значение для перечисления.</span><span class="sxs-lookup"><span data-stu-id="42a48-168">The maximum value for the enum.</span></span> <span data-ttu-id="42a48-169">Его не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="42a48-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="42a48-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42a48-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42a48-171">Справочник</span><span class="sxs-lookup"><span data-stu-id="42a48-171">Reference</span></span>

[<span data-ttu-id="42a48-172">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="42a48-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
