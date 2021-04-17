---
description: Состояние питания системы указывает, является ли источник питания компьютера системным аккумулятором или питанием от сети. Для компьютеров, использующих батареи, состояние питания системы также указывает на то, сколько времени работы батареи остается, и от того, заряжается ли батарея.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Состояние питания системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673792"
---
# <a name="system-power-status"></a><span data-ttu-id="32b5a-104">Состояние питания системы</span><span class="sxs-lookup"><span data-stu-id="32b5a-104">System Power Status</span></span>

<span data-ttu-id="32b5a-105">Состояние питания системы указывает, является ли источник питания компьютера системным аккумулятором или питанием от сети.</span><span class="sxs-lookup"><span data-stu-id="32b5a-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="32b5a-106">Для компьютеров, использующих батареи, состояние питания системы также указывает на то, сколько времени работы батареи остается, и от того, заряжается ли батарея.</span><span class="sxs-lookup"><span data-stu-id="32b5a-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="32b5a-107">Сведения о питании извлекаются путем регистрации уведомлений о параметрах питания с помощью функции [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) .</span><span class="sxs-lookup"><span data-stu-id="32b5a-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="32b5a-108">Эта функция позволяет приложениям регистрироваться на определенные параметры питания и получать уведомления при их изменении.</span><span class="sxs-lookup"><span data-stu-id="32b5a-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="32b5a-109">Чтобы запросить сведения о состоянии питания без уведомлений, используйте [**каллнтповеринформатион**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span><span class="sxs-lookup"><span data-stu-id="32b5a-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="32b5a-110">Приложения и устанавливаемые драйверы обычно используют системное состояние питания, чтобы определить, является ли продолжение операции возможным.</span><span class="sxs-lookup"><span data-stu-id="32b5a-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="32b5a-111">Например, прежде чем приложение выполняет фоновые операции, такие как сжатие или разбивка файла, оно должно проверить, находится ли система на аккумуляторах.</span><span class="sxs-lookup"><span data-stu-id="32b5a-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="32b5a-112">Другой пример: приложение, которое начинает длительную операцию, должно проверить состояние, чтобы определить, существует ли достаточно энергии аккумулятора для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="32b5a-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="32b5a-113">По умолчанию система не запрашивает приложения или драйверы во время переходов спящего режима.</span><span class="sxs-lookup"><span data-stu-id="32b5a-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="32b5a-114">Если уровень питания низкий, приложение может запросить вмешательство пользователя или запросить, что система приостанавливает работу.</span><span class="sxs-lookup"><span data-stu-id="32b5a-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="32b5a-115">Можно приостановить работу системы с помощью функции [**сетсуспендстате**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="32b5a-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="32b5a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="32b5a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32b5a-117">Сведения об управлении питанием</span><span class="sxs-lookup"><span data-stu-id="32b5a-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



