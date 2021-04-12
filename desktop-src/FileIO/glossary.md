---
description: Терминология, используемая для описания транзакционной NTFS (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Глоссарий TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272276"
---
# <a name="txf-glossary"></a><span data-ttu-id="5a105-103">Глоссарий TxF</span><span class="sxs-lookup"><span data-stu-id="5a105-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="5a105-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**ресурс**</span><span class="sxs-lookup"><span data-stu-id="5a105-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="5a105-105">Доступность означает, что диспетчер ресурсов будет прерывать транзакции, даже если это приведет к нарушению согласованности, что позволит системе продолжить новую работу.</span><span class="sxs-lookup"><span data-stu-id="5a105-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="5a105-106">Диспетчер ресурсов по умолчанию принудительно записывает доступность на системном томе.</span><span class="sxs-lookup"><span data-stu-id="5a105-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="5a105-107">Например, если журнал транзакций полон, то новое пространство журнала транзакций не может быть добавлено, а более старая транзакция, которая будет прервана, требует передачи из старшего диспетчера ресурсов для завершения распределенной транзакции. Диспетчер ресурсов не ожидает старший диспетчер транзакций и не прерывает эту транзакцию, несмотря на то, что может привести к нарушению согласованности.</span><span class="sxs-lookup"><span data-stu-id="5a105-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="5a105-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**согласованности**</span><span class="sxs-lookup"><span data-stu-id="5a105-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="5a105-109">Согласованность означает, что диспетчер ресурсов не сможет создать новые транзакции, если он не сможет выполнить пересылку.</span><span class="sxs-lookup"><span data-stu-id="5a105-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="5a105-110">Например, если журнал транзакций полон, Добавление нового пространства журнала транзакций невозможно, а более старая транзакция, которая будет прервана, требует передачи из старшего диспетчера ресурсов, чтобы выполнить распределенную транзакцию, диспетчер ресурсов будет ожидать этого результата.</span><span class="sxs-lookup"><span data-stu-id="5a105-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="5a105-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**Версия**</span><span class="sxs-lookup"><span data-stu-id="5a105-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="5a105-112">Мини-версия представляет собой версию файла, которая создается транзакционным модулем записи во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="5a105-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="5a105-113">Мини-версию можно открыть позже в транзакции с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5a105-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="5a105-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**Транзакционное средство чтения**</span><span class="sxs-lookup"><span data-stu-id="5a105-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="5a105-115">Транзакционное средство чтения — это транзакционный файловый обработчик, Открытый с любым разрешением, который является частью универсального доступа для чтения, но не является частью универсального доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="5a105-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="5a105-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**Транзакционный модуль записи**</span><span class="sxs-lookup"><span data-stu-id="5a105-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="5a105-117">Транзакционный модуль записи — это транзакционный файловый обработчик, Открытый с любым разрешением, которое не является частью универсального доступа для чтения, но является частью универсального доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="5a105-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 



