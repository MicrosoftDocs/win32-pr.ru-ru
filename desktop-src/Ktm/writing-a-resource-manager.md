---
description: При написании службы или компонента и необходимости использования служб транзакций или при необходимости наблюдения за состоянием транзакций ядра необходимо создать диспетчер ресурсов (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Запись диспетчер ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673596"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="39b84-103">Запись диспетчер ресурсов</span><span class="sxs-lookup"><span data-stu-id="39b84-103">Writing a Resource Manager</span></span>

<span data-ttu-id="39b84-104">При написании службы или компонента и необходимости использования служб транзакций или при необходимости наблюдения за состоянием транзакций ядра необходимо создать диспетчер ресурсов (RM).</span><span class="sxs-lookup"><span data-stu-id="39b84-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="39b84-105">Для создания диспетчера ресурсов необходимо создать несколько объектов ядра.</span><span class="sxs-lookup"><span data-stu-id="39b84-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="39b84-106">Объекты, используемые диспетчером ресурсов:</span><span class="sxs-lookup"><span data-stu-id="39b84-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="39b84-107">Объекты диспетчера транзакций (TM)</span><span class="sxs-lookup"><span data-stu-id="39b84-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="39b84-108">диспетчер ресурсов объекты</span><span class="sxs-lookup"><span data-stu-id="39b84-108">Resource Manager objects</span></span>
-   <span data-ttu-id="39b84-109">Объекты зачислений</span><span class="sxs-lookup"><span data-stu-id="39b84-109">Enlistment objects</span></span>

<span data-ttu-id="39b84-110">Сначала создайте объект TM.</span><span class="sxs-lookup"><span data-stu-id="39b84-110">First, create a TM object.</span></span> <span data-ttu-id="39b84-111">Существует два типа TMs:</span><span class="sxs-lookup"><span data-stu-id="39b84-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="39b84-112">Volatile — эти TMs не имеют журнала и не могут восстановить их состояние.</span><span class="sxs-lookup"><span data-stu-id="39b84-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="39b84-113">Устойчивый — у этих TMs есть журнал</span><span class="sxs-lookup"><span data-stu-id="39b84-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="39b84-114">Чтобы создать устойчивый TM-диспетчер, необходимо создать журнал CLFS и вызвать [**креатетрансактионманажер**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) или создать его для вас с помощью KTM.</span><span class="sxs-lookup"><span data-stu-id="39b84-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="39b84-115">После создания долговременного TM необходимо сначала восстановить TM, вызвав [**рековертрансактионманажер**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span><span class="sxs-lookup"><span data-stu-id="39b84-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="39b84-116">После восстановления TM она становится доступной для использования.</span><span class="sxs-lookup"><span data-stu-id="39b84-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="39b84-117">Если вы восстановили существующий TM, все RMs, связанные с этим TM, начнут получать сообщения о восстановлении.</span><span class="sxs-lookup"><span data-stu-id="39b84-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="39b84-118">Дополнительные сведения см. в разделе [Обработка восстановления](recovery-processing.md).</span><span class="sxs-lookup"><span data-stu-id="39b84-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="39b84-119">Затем создайте диспетчер ресурсов, вызвав [**креатересаурцеманажер**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) с помощью обработчика TM.</span><span class="sxs-lookup"><span data-stu-id="39b84-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="39b84-120">RM может быть энергозависимой или устойчивой.</span><span class="sxs-lookup"><span data-stu-id="39b84-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="39b84-121">С устойчивым RMs можно использовать только устойчивый TMs.</span><span class="sxs-lookup"><span data-stu-id="39b84-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="39b84-122">При работе с транзакционными операциями вы присоединяете транзакцию, вызывая [**креатинлистмент**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)и указывая, какие уведомления следует получать.</span><span class="sxs-lookup"><span data-stu-id="39b84-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="39b84-123">**Примечание**  .  Вы можете начать получать уведомления до завершения вызова [**креатинлистмент**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .</span><span class="sxs-lookup"><span data-stu-id="39b84-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="39b84-124">При получении уведомления вызовите соответствующую функцию Complete, \* когда завершится любая работа, связанная с обработкой уведомления.</span><span class="sxs-lookup"><span data-stu-id="39b84-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="39b84-125">Полные функции:</span><span class="sxs-lookup"><span data-stu-id="39b84-125">The complete functions are:</span></span>

-   [<span data-ttu-id="39b84-126">**коммиткомплете**</span><span class="sxs-lookup"><span data-stu-id="39b84-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="39b84-127">**препарекомплете**</span><span class="sxs-lookup"><span data-stu-id="39b84-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="39b84-128">**препрепарекомплете**</span><span class="sxs-lookup"><span data-stu-id="39b84-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="39b84-129">Если в любой момент, когда диспетчер ресурсов не сможет завершить работу транзакции или если продолжить, приложение не сможет отменить работу, выполненную в рамках транзакции, необходимо выполнить откат транзакции, вызвав [**роллбаккенлистмент**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span><span class="sxs-lookup"><span data-stu-id="39b84-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 



