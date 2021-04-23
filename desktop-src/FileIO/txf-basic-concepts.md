---
description: Описывает согласованность с фиксированной нагрузкой, изоляцию с фиксированным чтением и понятия блокировки транзакций в транзакционной NTFS.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Основные понятия TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347822"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="0ce77-103">Основные понятия TxF</span><span class="sxs-lookup"><span data-stu-id="0ce77-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="0ce77-104">Изоляция чтения</span><span class="sxs-lookup"><span data-stu-id="0ce77-104">Read Isolation</span></span>

<span data-ttu-id="0ce77-105">Транзакционная NTFS (TxF) обеспечивает согласованность чтения и фиксации.</span><span class="sxs-lookup"><span data-stu-id="0ce77-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="0ce77-106">[*Транзакционный модуль записи*](glossary.md) ссылается на транзакционный файловый обработчик, Открытый с любым разрешением, которое не является частью универсального доступа для чтения, но является частью универсального доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="0ce77-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="0ce77-107">*Транзакционный модуль записи* позволяет просматривать последнюю версию файла, включающую все изменения одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="0ce77-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="0ce77-108">Для одного файла может существовать только один транзакционный модуль записи.</span><span class="sxs-lookup"><span data-stu-id="0ce77-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="0ce77-109">Модули записи, не поддерживающие транзакции, всегда блокируются транзакционным модулем записи, даже если файл открыт с разрешениями общего доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="0ce77-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="0ce77-110">[*Транзакционный читатель*](glossary.md) ссылается на транзакционный файловый обработчик, Открытый с любым разрешением, которое является частью универсального доступа для чтения, но не является частью универсального доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="0ce77-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="0ce77-111">*Транзакционный считыватель* просматривает зафиксированную версию файла, существовавшую на момент открытия этого маркера файла.</span><span class="sxs-lookup"><span data-stu-id="0ce77-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="0ce77-112">Транзакционный модуль чтения изолирован от влияния транзакционных модулей записи.</span><span class="sxs-lookup"><span data-stu-id="0ce77-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="0ce77-113">Это обеспечивает единообразное представление файла только в течение жизненного цикла обработчика файла и блокирует нетранзакционные модули записи.</span><span class="sxs-lookup"><span data-stu-id="0ce77-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="0ce77-114">При открытии обработчика для изменения с помощью функции [**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) все последующие открытия файла в этой транзакции записываются независимо от того, преобразуются ли система в транзакционный модуль записи в целях изоляции и другой транзакционной семантики.</span><span class="sxs-lookup"><span data-stu-id="0ce77-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="0ce77-115">Это означает, что при открытии обработчика для доступа только для чтения этот обработчик не получает представление файла до начала транзакции. он получает активное представление транзакций файла.</span><span class="sxs-lookup"><span data-stu-id="0ce77-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="0ce77-116">Нетранзакционный файловый обработчик не увидит никаких изменений, внесенных в транзакцию, пока транзакция не будет зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="0ce77-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="0ce77-117">Нетранзакционный файловый обработчик получает изолированное представление, похожее на транзакционное средство чтения, но в отличие от транзакционного чтения, оно получает обновление файла, когда транзакционный модуль записи фиксирует транзакцию.</span><span class="sxs-lookup"><span data-stu-id="0ce77-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="0ce77-118">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="0ce77-118">Isolation Levels</span></span>

<span data-ttu-id="0ce77-119">TxF обеспечивает изоляцию READ COMMITTED.</span><span class="sxs-lookup"><span data-stu-id="0ce77-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="0ce77-120">Это означает, что обновления файлов не видны за пределами транзакции.</span><span class="sxs-lookup"><span data-stu-id="0ce77-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="0ce77-121">Кроме того, если файл открывается более одного раза при чтении файлов в рамках транзакции, то при каждом последующем открытии могут отображаться разные результаты.</span><span class="sxs-lookup"><span data-stu-id="0ce77-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="0ce77-122">Файлы, которые были доступны при первом обращении к ним, могут быть недоступны (поскольку они были удалены) или наоборот.</span><span class="sxs-lookup"><span data-stu-id="0ce77-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="0ce77-123">Транзакционная блокировка</span><span class="sxs-lookup"><span data-stu-id="0ce77-123">Transactional Locking</span></span>

<span data-ttu-id="0ce77-124">Создание транзакционного модуля записи в файле *блокирует* файл.</span><span class="sxs-lookup"><span data-stu-id="0ce77-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="0ce77-125">После того как файл заблокирован транзакцией, другие операции файловой системы, которые являются внешними для транзакции блокировки, которые пытаются изменить транзакционно заблокированный файл, завершатся сбоем с **\_ \_ нарушением общего доступа к ошибкам** или **\_ \_ конфликтом транзакций с ошибками**.</span><span class="sxs-lookup"><span data-stu-id="0ce77-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="0ce77-126">В следующей таблице приводится сводка блокировок транзакций.</span><span class="sxs-lookup"><span data-stu-id="0ce77-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="0ce77-127">Файл, Открытый в настоящий момент</span><span class="sxs-lookup"><span data-stu-id="0ce77-127">File currently opened by</span></span>

<span data-ttu-id="0ce77-128">Предпринята ошибка при открытии файла</span><span class="sxs-lookup"><span data-stu-id="0ce77-128">File open attempted by</span></span>

<span data-ttu-id="0ce77-129">С транзакцией</span><span class="sxs-lookup"><span data-stu-id="0ce77-129">Transacted</span></span>

<span data-ttu-id="0ce77-130">Без транзакции</span><span class="sxs-lookup"><span data-stu-id="0ce77-130">Non-Transacted</span></span>

<span data-ttu-id="0ce77-131">Читатель</span><span class="sxs-lookup"><span data-stu-id="0ce77-131">Reader</span></span>

<span data-ttu-id="0ce77-132">Модуль чтения/записи</span><span class="sxs-lookup"><span data-stu-id="0ce77-132">Reader/Writer</span></span>

<span data-ttu-id="0ce77-133">Читатель</span><span class="sxs-lookup"><span data-stu-id="0ce77-133">Reader</span></span>

<span data-ttu-id="0ce77-134">Модуль чтения/записи</span><span class="sxs-lookup"><span data-stu-id="0ce77-134">Reader/Writer</span></span>

<span data-ttu-id="0ce77-135">Транзакционное средство чтения</span><span class="sxs-lookup"><span data-stu-id="0ce77-135">Transacted Reader</span></span>

<span data-ttu-id="0ce77-136">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-136">Yes</span></span>

<span data-ttu-id="0ce77-137">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-137">Yes</span></span>

<span data-ttu-id="0ce77-138">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-138">Yes</span></span>

<span data-ttu-id="0ce77-139">Нет2</span><span class="sxs-lookup"><span data-stu-id="0ce77-139">No2</span></span>

<span data-ttu-id="0ce77-140">Транзакционный поток чтения/записи</span><span class="sxs-lookup"><span data-stu-id="0ce77-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="0ce77-141">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-141">Yes</span></span>

<span data-ttu-id="0ce77-142">Нет2</span><span class="sxs-lookup"><span data-stu-id="0ce77-142">No2</span></span>

<span data-ttu-id="0ce77-143">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-143">Yes</span></span>

<span data-ttu-id="0ce77-144">Нет2</span><span class="sxs-lookup"><span data-stu-id="0ce77-144">No2</span></span>

<span data-ttu-id="0ce77-145">Модуль чтения, не поддерживающий транзакции</span><span class="sxs-lookup"><span data-stu-id="0ce77-145">Non-Transacted Reader</span></span>

<span data-ttu-id="0ce77-146">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-146">Yes</span></span>

<span data-ttu-id="0ce77-147">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-147">Yes</span></span>

<span data-ttu-id="0ce77-148">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-148">Yes</span></span>

<span data-ttu-id="0ce77-149">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-149">Yes</span></span>

<span data-ttu-id="0ce77-150">Не транзакционный поток чтения/записи</span><span class="sxs-lookup"><span data-stu-id="0ce77-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="0ce77-151">Нет1</span><span class="sxs-lookup"><span data-stu-id="0ce77-151">No1</span></span>

<span data-ttu-id="0ce77-152">Нет1</span><span class="sxs-lookup"><span data-stu-id="0ce77-152">No1</span></span>

<span data-ttu-id="0ce77-153">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-153">Yes</span></span>

<span data-ttu-id="0ce77-154">Да</span><span class="sxs-lookup"><span data-stu-id="0ce77-154">Yes</span></span>

1. <span data-ttu-id="0ce77-155">Завершается ошибкой с **\_ \_ конфликтом транзакций**</span><span class="sxs-lookup"><span data-stu-id="0ce77-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="0ce77-156">2. сбой с **\_ \_ нарушением совместного использования ошибок**</span><span class="sxs-lookup"><span data-stu-id="0ce77-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="0ce77-157">При открытии именованного потока для изменения, которое использует транзакцию, весь файл должен быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="0ce77-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="0ce77-158">Помимо транзакционной блокировки применяются обычные правила общего доступа к файлам NTFS.</span><span class="sxs-lookup"><span data-stu-id="0ce77-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="0ce77-159">В параллельном режиме необходимо учитывать два следующих режима совместного использования файлов:</span><span class="sxs-lookup"><span data-stu-id="0ce77-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="0ce77-160">Режим блокировки транзакций.</span><span class="sxs-lookup"><span data-stu-id="0ce77-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="0ce77-161">Нормальные режимы совместного использования файлов.</span><span class="sxs-lookup"><span data-stu-id="0ce77-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="0ce77-162">Какой-либо режим является более узким, который применяется.</span><span class="sxs-lookup"><span data-stu-id="0ce77-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 




