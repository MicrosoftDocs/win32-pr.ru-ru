---
description: Транзакция — это ряд изменений хранилища данных (например, базы данных или файловой системы), которые гарантированно выполняются успешно или не выполняются вообще.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Транзакционная очередь сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4730b20f4014cdf7c76462d3f2cae272695d907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072417"
---
# <a name="transactional-message-queuing"></a><span data-ttu-id="98dad-103">Транзакционная очередь сообщений</span><span class="sxs-lookup"><span data-stu-id="98dad-103">Transactional Message Queuing</span></span>

<span data-ttu-id="98dad-104">*Транзакция* — это ряд изменений хранилища данных (например, базы данных или файловой системы), которые гарантированно выполняются успешно или не выполняются вообще.</span><span class="sxs-lookup"><span data-stu-id="98dad-104">A *transaction* is a series of modifications of a data store (such as a database or a file system) guaranteed either to be all successfully executed or not to be executed at all.</span></span> <span data-ttu-id="98dad-105">Чтобы реализовать транзакцию, запись сохраняется в состоянии хранилища данных до начала транзакции и, если одно из изменений завершается неудачей, транзакция возвращает ошибку, а начальное состояние восстанавливается (или откатывается).</span><span class="sxs-lookup"><span data-stu-id="98dad-105">To implement a transaction, a record is kept of the state of the data store before the transaction begins and, if one of the modifications fails, the transaction returns failure and the initial state is restored (or rolled back).</span></span> <span data-ttu-id="98dad-106">Транзакции используются для поддержания целостности данных и, следовательно, играют важную роль в программировании бизнес-программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="98dad-106">Transactions are used to maintain data integrity and consequently play an important role in business software programming.</span></span>

<span data-ttu-id="98dad-107">Часто приложения можно разрабатывать с помощью бизнес-транзакции или рабочего процесса, разбитого на несколько небольших транзакций или действий.</span><span class="sxs-lookup"><span data-stu-id="98dad-107">Often, applications can be developed using a business transaction or workflow that is split into several smaller transactions or activities.</span></span> <span data-ttu-id="98dad-108">Эти действия разделяются по времени, а затем соединяются с помощью надежных очередей сообщений.</span><span class="sxs-lookup"><span data-stu-id="98dad-108">These activities are separated in time and then connected using reliable message queues.</span></span>

1.  <span data-ttu-id="98dad-109">Первая транзакция включает в себя базу данных ввода заказа.</span><span class="sxs-lookup"><span data-stu-id="98dad-109">The first transaction involves the order entry database.</span></span> <span data-ttu-id="98dad-110">[Очередь сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) перемещает сообщение из одной очереди в другую, только один раз, используя возможности транзакций.</span><span class="sxs-lookup"><span data-stu-id="98dad-110">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) moves the message from one queue to another queue, exactly one time, using transaction capabilities.</span></span> <span data-ttu-id="98dad-111">Если база данных обновляется, в очереди появляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="98dad-111">If the database is updated, there is a message on the queue.</span></span> <span data-ttu-id="98dad-112">Если сообщение не достигает очереди, оно прерывается и выполняется откат базы данных.</span><span class="sxs-lookup"><span data-stu-id="98dad-112">If the message doesn't reach the queue, it is aborted and the database is rolled back.</span></span>
2.  <span data-ttu-id="98dad-113">Позже очередь сообщений обнаружит, что сервер доступен.</span><span class="sxs-lookup"><span data-stu-id="98dad-113">Sometime later, Message Queuing discovers that the server is available.</span></span> <span data-ttu-id="98dad-114">Нет опросов приложений на наличие сервера.</span><span class="sxs-lookup"><span data-stu-id="98dad-114">There is no application polling for the existence of the server.</span></span> <span data-ttu-id="98dad-115">Это вторая транзакция.</span><span class="sxs-lookup"><span data-stu-id="98dad-115">This is the second transaction.</span></span>
3.  <span data-ttu-id="98dad-116">Третья транзакция включает в себя запрос на доставку базы данных и обновление базы данных доставки.</span><span class="sxs-lookup"><span data-stu-id="98dad-116">The third transaction involves a shipping database query and the update of the shipping database.</span></span> <span data-ttu-id="98dad-117">В случае сбоя сервера в ходе этой транзакции происходит откат изменений и сообщение возвращается в очередь ввода.</span><span class="sxs-lookup"><span data-stu-id="98dad-117">If the server fails in the middle of this transaction, the modification is rolled back and the message is returned to the input queue.</span></span> <span data-ttu-id="98dad-118">Это гарантирует, что целостность данных и базы данных будет поддерживаться во время транзакций.</span><span class="sxs-lookup"><span data-stu-id="98dad-118">This ensures that the integrity of the data and databases is maintained during the transactions.</span></span>

 

 



