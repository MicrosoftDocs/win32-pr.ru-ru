---
title: Функции планирования
description: Функции службы расписания управления сетью отправляют задания, которые выполняются на указанном компьютере в определенное время (или раз) в определенный момент времени в будущем, и управляют ими.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672375"
---
# <a name="schedule-functions"></a><span data-ttu-id="d1006-103">Функции планирования</span><span class="sxs-lookup"><span data-stu-id="d1006-103">Schedule Functions</span></span>

<span data-ttu-id="d1006-104">Функции службы расписания управления сетью отправляют задания, которые выполняются на указанном компьютере в определенное время (или раз) в определенный момент времени в будущем, и управляют ими.</span><span class="sxs-lookup"><span data-stu-id="d1006-104">The network management schedule service functions submit and manage jobs that execute on a specified computer at a particular time (or times) in the future.</span></span> <span data-ttu-id="d1006-105">Задания могут включать команды и программы.</span><span class="sxs-lookup"><span data-stu-id="d1006-105">Jobs can include commands and programs.</span></span> <span data-ttu-id="d1006-106">Функции управляют заданиями на удаленных и локальных компьютерах при условии, что на компьютере запущена служба расписания.</span><span class="sxs-lookup"><span data-stu-id="d1006-106">The functions manage jobs at remote and local computers, provided the schedule service is running on the computer.</span></span>

<span data-ttu-id="d1006-107">Ниже перечислены функции службы расписания.</span><span class="sxs-lookup"><span data-stu-id="d1006-107">The schedule service functions are listed following.</span></span>



| <span data-ttu-id="d1006-108">Функция</span><span class="sxs-lookup"><span data-stu-id="d1006-108">Function</span></span>                                                                     | <span data-ttu-id="d1006-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d1006-109">Description</span></span>                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="d1006-110">**нетсчедулежобадд**</span><span class="sxs-lookup"><span data-stu-id="d1006-110">**NetScheduleJobAdd**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | <span data-ttu-id="d1006-111">Отправляет задание для выполнения в указанную будущую дату и время.</span><span class="sxs-lookup"><span data-stu-id="d1006-111">Submits a job to run at a specified future date and time.</span></span>        |
| [<span data-ttu-id="d1006-112">**нетсчедулежобдел**</span><span class="sxs-lookup"><span data-stu-id="d1006-112">**NetScheduleJobDel**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | <span data-ttu-id="d1006-113">Отменяет ряд заданий, поставленных в очередь для запуска на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1006-113">Cancels a range of jobs queued to run on a computer.</span></span>             |
| [<span data-ttu-id="d1006-114">**нетсчедулежобенум**</span><span class="sxs-lookup"><span data-stu-id="d1006-114">**NetScheduleJobEnum**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | <span data-ttu-id="d1006-115">Список заданий, поставленных в очередь на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1006-115">Lists the jobs queued on a specified computer.</span></span>                   |
| [<span data-ttu-id="d1006-116">**нетсчедулежобжетинфо**</span><span class="sxs-lookup"><span data-stu-id="d1006-116">**NetScheduleJobGetInfo**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | <span data-ttu-id="d1006-117">Возвращает сведения о конкретном задании, поставленном в очередь на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1006-117">Returns information about a particular job queued on a computer.</span></span> |
| [<span data-ttu-id="d1006-118">**жетнетсчедулеаккаунтинформатион**</span><span class="sxs-lookup"><span data-stu-id="d1006-118">**GetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | <span data-ttu-id="d1006-119">Возвращает имя учетной записи службы AT.</span><span class="sxs-lookup"><span data-stu-id="d1006-119">Retrieves the AT Service account name.</span></span>                           |
| [<span data-ttu-id="d1006-120">**сетнетсчедулеаккаунтинформатион**</span><span class="sxs-lookup"><span data-stu-id="d1006-120">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | <span data-ttu-id="d1006-121">Задает имя учетной записи службы AT и пароль.</span><span class="sxs-lookup"><span data-stu-id="d1006-121">Sets the AT Service account name and password.</span></span>                   |



 

<span data-ttu-id="d1006-122">Чтобы успешно выполнить функции расписания управления сетью, вызывающая сторона должна иметь права администратора на компьютере, на котором запущена служба расписания.</span><span class="sxs-lookup"><span data-stu-id="d1006-122">For the network management schedule functions to succeed, a caller must have administrator's privilege at the computer where the schedule service is running.</span></span> <span data-ttu-id="d1006-123">Функции службы расписания также называются функциями "задание" и "команда AT".</span><span class="sxs-lookup"><span data-stu-id="d1006-123">The schedule service functions are also known as "Job" and "AT command" functions.</span></span> <span data-ttu-id="d1006-124">Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="d1006-124">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="d1006-125">Структура [**\_ info**](/windows/desktop/api/Lmat/ns-lmat-at_info) используется функцией [**нетсчедулежобадд**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) для указания информации при отправке задания и функции [**нетсчедулежобжетинфо**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) для получения сведений о задании, которое было отправлено.</span><span class="sxs-lookup"><span data-stu-id="d1006-125">The [**AT\_INFO**](/windows/desktop/api/Lmat/ns-lmat-at_info) structure is used by the [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) function to specify information when submitting a job, and by the [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) function to retrieve information about a job that has been submitted.</span></span> <span data-ttu-id="d1006-126">Структура [**в \_ enum**](/windows/desktop/api/Lmat/ns-lmat-at_enum) используется [**нетсчедулежобенум**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) для перечисления и возврата сведений о всей очереди отправленных заданий.</span><span class="sxs-lookup"><span data-stu-id="d1006-126">The [**AT\_ENUM**](/windows/desktop/api/Lmat/ns-lmat-at_enum) structure is used by [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) to enumerate and return information about an entire queue of submitted jobs.</span></span>

 

 