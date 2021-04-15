---
title: Завершение задания и его отмена
description: Чтобы завершить задание перемещения, вызовите метод использованием метода ibackgroundcopyjob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- передачи битов задания, отмена
- Отмена битов задания
- БИТЫ заданий передачи, завершение
- завершение битов задания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486652"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="aa071-107">Завершение задания и его отмена</span><span class="sxs-lookup"><span data-stu-id="aa071-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="aa071-108">Чтобы завершить задание перемещения, вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="aa071-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="aa071-109">Для заданий загрузки можно вызвать метод **Complete** до передачи всех файлов в задании (до того, как состояние задания передано в состояние задания BG \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="aa071-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="aa071-110">Пользователю будут доступны только те файлы, которые были успешно переданы клиенту службой BITS до вызова метода **Complete** .</span><span class="sxs-lookup"><span data-stu-id="aa071-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="aa071-111">Для заданий отправки вызовите метод [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) только в том случае, если состояние задания — \_ « \_ Передача состояния задания BG» \_ .</span><span class="sxs-lookup"><span data-stu-id="aa071-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="aa071-112">Чтобы определить, когда состояние задания — \_ \_ передано состояние задания BG \_ , следует [опросить](polling-for-the-status-of-the-job.md) свойство состояния задания или зарегистрировать, чтобы получить \_ уведомление о \_ \_ [событии](registering-a-com-callback.md)переданного задания в BG.</span><span class="sxs-lookup"><span data-stu-id="aa071-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="aa071-113">Чтобы отменить задание на перемещение, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="aa071-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="aa071-114">Метод **Cancel** удаляет задание из очереди на перемещение и удаляет временные файлы с клиента.</span><span class="sxs-lookup"><span data-stu-id="aa071-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="aa071-115">Как правило, этот метод вызывается, если не удается разрешить ошибку, связанную с заданием.</span><span class="sxs-lookup"><span data-stu-id="aa071-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="aa071-116">Метод [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) отменяет отправку, если передача не завершена.</span><span class="sxs-lookup"><span data-stu-id="aa071-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="aa071-117">Если передача завершена, а задание имеет тип \_ задания BG \_ \_ upload \_ , метод отменяет ответ.</span><span class="sxs-lookup"><span data-stu-id="aa071-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="aa071-118">Если не вызвать метод [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) или метод [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) в течение 90 дней (по умолчанию [жобинактивититимеаут](group-policies.md) групповая политика), служба отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="aa071-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="aa071-119">Если служба отменяет задание, скачанные файлы и файл ответов недоступны для клиента. Отмена заданий не влияет на успешно отправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="aa071-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="aa071-120">Следует всегда вызывать метод **Complete** или **Cancel** и не полагаться на политику жобинактивититимеаут для очистки заданий.</span><span class="sxs-lookup"><span data-stu-id="aa071-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="aa071-121">Задания, оставшиеся в очереди, могут помешать пользователям создавать другие задания при достижении предела политики Maxjobspermachine или MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="aa071-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 




