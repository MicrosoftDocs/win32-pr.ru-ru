---
description: 'Дополнительные сведения: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702358"
---
# <a name="jet_errcat"></a><span data-ttu-id="49829-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="49829-103">JET_ERRCAT</span></span>


<span data-ttu-id="49829-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49829-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="49829-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="49829-105">JET_ERRCAT</span></span>

<span data-ttu-id="49829-106">**JET_ERRCAT** группа констант описывает классификацию более высокого уровня или категории ошибок.</span><span class="sxs-lookup"><span data-stu-id="49829-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="49829-107">Эта группа констант позволяет приложениям определять обработку по умолчанию для классификации ошибок, а не обрабатывать каждый случай возникновения ошибки по отдельности.</span><span class="sxs-lookup"><span data-stu-id="49829-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="49829-108">Это также гарантирует, что приложению не требуется обработка новых условий ошибок, которые включены в существующие классификации.</span><span class="sxs-lookup"><span data-stu-id="49829-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="49829-109">Примечание. Эта документация основана на предварительном выпуске расширяемой подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="49829-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="49829-110">Эта информация может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="49829-110">This information is subject to change.</span></span>

<span data-ttu-id="49829-111">**JET_ERRCAT** константы упорядочиваются в определенной иерархии условий и подусловий следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49829-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="49829-112">|---Ошибка |---операцию (Al) | |---Неустранимая операция | |---IO | | ресурс | |---памяти | | квота | |---диска | |---данных | |---повреждений | |---несогласованности | |---фрагментации | |---API | использование | состояние---</span><span class="sxs-lookup"><span data-stu-id="49829-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="49829-113">В следующей таблице перечислены **JET_ERRCAT** константы и предоставлены сведения об их описании и восстановлении.</span><span class="sxs-lookup"><span data-stu-id="49829-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49829-114">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="49829-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="49829-115">Описание</span><span class="sxs-lookup"><span data-stu-id="49829-115">Description</span></span></p></th>
<th><p><span data-ttu-id="49829-116">Восстановление</span><span class="sxs-lookup"><span data-stu-id="49829-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49829-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="49829-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="49829-118">Недопустимая Категория ошибки.</span><span class="sxs-lookup"><span data-stu-id="49829-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="49829-119">Недоступно</span><span class="sxs-lookup"><span data-stu-id="49829-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="49829-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="49829-121">Категория верхнего уровня (ошибки не должны относиться к этому классу).</span><span class="sxs-lookup"><span data-stu-id="49829-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="49829-122">Ознакомьтесь с конкретными константами ошибок.</span><span class="sxs-lookup"><span data-stu-id="49829-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="49829-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="49829-124">Представляет ошибки, которые могут возникать в любое время из-за условий неконтролируемых и часто являются временными.</span><span class="sxs-lookup"><span data-stu-id="49829-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="49829-125">См. раздел подкатегории, если они указаны.</span><span class="sxs-lookup"><span data-stu-id="49829-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="49829-126">Повторите попытку. Если ошибка повторится, сообщите оператору.</span><span class="sxs-lookup"><span data-stu-id="49829-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="49829-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="49829-128">Представляет неустранимые ошибки, которые, когда они возникают, создают риск того, что ESE не может продолжать работу в безопасном (часто транзакционном) способе, и данные могут быть повреждены.</span><span class="sxs-lookup"><span data-stu-id="49829-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="49829-129">Перезапустите экземпляр или процесс.</span><span class="sxs-lookup"><span data-stu-id="49829-129">Restart the instance or process.</span></span> <span data-ttu-id="49829-130">Если проблема повторяется, сообщите оператору.</span><span class="sxs-lookup"><span data-stu-id="49829-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="49829-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="49829-132">Представляет ошибки ввода-вывода, которые поступают от операционной системы и выходят за пределы элемента управления ESE.</span><span class="sxs-lookup"><span data-stu-id="49829-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="49829-133">Этот тип ошибки может быть временным.</span><span class="sxs-lookup"><span data-stu-id="49829-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="49829-134">Повторите попытку. Если ошибка повторится, попросите оператора проверить диск.</span><span class="sxs-lookup"><span data-stu-id="49829-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="49829-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="49829-136">Представляет категорию ошибок, связанных с отсутствием условий ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49829-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="49829-137">См. раздел подкатегории.</span><span class="sxs-lookup"><span data-stu-id="49829-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="49829-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="49829-139">Представляет ошибку, вызванную нехваткой памяти.</span><span class="sxs-lookup"><span data-stu-id="49829-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="49829-140">Повторите попытку через некоторое время, освободите память или завершите работу.</span><span class="sxs-lookup"><span data-stu-id="49829-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="49829-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="49829-142">Некоторые &quot; специализированные &quot; ресурсы находятся в пулах определенного размера, что упрощает обнаружение утечек этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49829-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="49829-143">Приложение должно <strong>утверждать ()</strong> для обнаружения этих проблем во время разработки.</span><span class="sxs-lookup"><span data-stu-id="49829-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="49829-144">Однако в розничном коде приложение должно обрабатывать это как ошибку памяти.</span><span class="sxs-lookup"><span data-stu-id="49829-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="49829-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="49829-146">Представляет ошибку, вызванную недостатком места на диске.</span><span class="sxs-lookup"><span data-stu-id="49829-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="49829-147">Повторите попытку позже, чтобы определить, доступно ли дополнительное место на диске, или попросите оператора освободить место на диске.</span><span class="sxs-lookup"><span data-stu-id="49829-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="49829-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="49829-149">Представляет категорию верхнего уровня для ошибок, связанных с данными.</span><span class="sxs-lookup"><span data-stu-id="49829-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="49829-150">См. раздел подкатегории.</span><span class="sxs-lookup"><span data-stu-id="49829-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="49829-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="49829-152">Представляет ошибку повреждения, которая часто является постоянной без корректирующих действий.</span><span class="sxs-lookup"><span data-stu-id="49829-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="49829-153">Восстановление из резервной копии с помощью операции исправления служебных программ ESE (эта операция восстанавливает только те данные, которые остались или теряются).</span><span class="sxs-lookup"><span data-stu-id="49829-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="49829-154">Кроме того, при использовании метода восстановления (Жетинит) можно выполнить восстановление, добавив возможность потери данных (Дополнительные сведения см. в разделе <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="49829-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="49829-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="49829-156">Представляет ошибку, в которой файлы базы данных и (или) журнала находятся в несогласованном состоянии и не могут быть выверены.</span><span class="sxs-lookup"><span data-stu-id="49829-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="49829-157">Эта ошибка может быть вызвана неисправностью обработки приложения или администратора.</span><span class="sxs-lookup"><span data-stu-id="49829-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="49829-158">Выполните восстановление из резервной копии с помощью операции исправления служебных программ ESE (которая восстанавливает только те данные, которые остались или теряются).</span><span class="sxs-lookup"><span data-stu-id="49829-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="49829-159">Кроме того, в случае операции <strong>восстановления (жетинит)</strong> восстановление можно выполнить, добавив возможность потери данных (Дополнительные сведения см. в разделе <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="49829-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="49829-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="49829-161">Представляет класс ошибок, в которых был запущен некоторый сохраненный внутренний ресурс.</span><span class="sxs-lookup"><span data-stu-id="49829-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="49829-162">В случае ошибок базы данных автономная дефрагментация устранит проблему.</span><span class="sxs-lookup"><span data-stu-id="49829-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="49829-163">Для файлов журнала сначала восстановите все подключенные базы данных до чистого завершения работы, а затем удалите все файлы журналов и контрольную точку.</span><span class="sxs-lookup"><span data-stu-id="49829-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="49829-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="49829-165">См. раздел подкатегории.</span><span class="sxs-lookup"><span data-stu-id="49829-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="49829-166">См. раздел подкатегории.</span><span class="sxs-lookup"><span data-stu-id="49829-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="49829-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="49829-168">Представляет ошибку использования.</span><span class="sxs-lookup"><span data-stu-id="49829-168">Represents a usage error.</span></span> <span data-ttu-id="49829-169">Код клиента не передает правильные аргументы в API <strong>Jet</strong> .</span><span class="sxs-lookup"><span data-stu-id="49829-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="49829-170">Эта ошибка будет сохранена с повторным выполнением.</span><span class="sxs-lookup"><span data-stu-id="49829-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="49829-171">Клиентский код должен использовать метод <strong>Assert ()</strong> , чтобы гарантировать, что этот класс ошибок не возвращается, поэтому проблемы могут быть перехвачены во время разработки.</span><span class="sxs-lookup"><span data-stu-id="49829-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="49829-172">В розничной торговле приложение должно уведомить оператора об ошибке.</span><span class="sxs-lookup"><span data-stu-id="49829-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="49829-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="49829-174">Представляет класс сообщений, которые могут возвращаться API для описания состояния базы данных.</span><span class="sxs-lookup"><span data-stu-id="49829-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="49829-175">Например, метод <a href="gg294103(v=exchg.10).md">жетсик ()</a> может возвращать <strong>JET_errRecordNotFound</strong> , если запрошенная запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="49829-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="49829-176">Зависит от API.</span><span class="sxs-lookup"><span data-stu-id="49829-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="49829-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="49829-178">Представляет ошибки из предыдущей версии подсистемы.</span><span class="sxs-lookup"><span data-stu-id="49829-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="49829-179">Текущая подсистема не должна возвращать эти ошибки.</span><span class="sxs-lookup"><span data-stu-id="49829-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="49829-180">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="49829-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="49829-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="49829-182">Константа, указывающая конец перечисления.</span><span class="sxs-lookup"><span data-stu-id="49829-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="49829-183">Недоступно</span><span class="sxs-lookup"><span data-stu-id="49829-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="49829-184">Требования</span><span class="sxs-lookup"><span data-stu-id="49829-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49829-185"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="49829-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49829-186">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49829-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49829-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="49829-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49829-188">Требуется Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="49829-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49829-189"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="49829-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49829-190">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="49829-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

