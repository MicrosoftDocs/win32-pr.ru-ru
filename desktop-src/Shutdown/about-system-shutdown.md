---
description: При завершении работы системы система переводится в состояние, в котором она может быть защищена от отключения компьютера.
ms.assetid: eeede4b3-8f68-4fe0-b16a-b5449aa27d59
title: О завершении работы системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590a062c5fcb252709ffd92bc2d6d7c8105571da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662845"
---
# <a name="about-system-shutdown"></a><span data-ttu-id="08a1c-103">О завершении работы системы</span><span class="sxs-lookup"><span data-stu-id="08a1c-103">About System Shutdown</span></span>

<span data-ttu-id="08a1c-104">При завершении работы системы система переводится в состояние, в котором она может быть защищена от отключения компьютера.</span><span class="sxs-lookup"><span data-stu-id="08a1c-104">System shutdown brings the system to a condition in which it is safe to turn off the computer.</span></span> <span data-ttu-id="08a1c-105">Все буферы файловой системы сбрасываются на диск, после чего появляется окно сообщения с сообщением о том, что компьютер может быть выключен.</span><span class="sxs-lookup"><span data-stu-id="08a1c-105">All file-system buffers are flushed to the disk, then a message box is displayed informing the user that the computer can be turned off.</span></span> <span data-ttu-id="08a1c-106">Существует также параметр reboot, который перезагружает компьютер, а не отображает окно сообщения о завершении работы системы.</span><span class="sxs-lookup"><span data-stu-id="08a1c-106">There is also a reboot option that will restart the computer, rather than display this system shutdown message box.</span></span> <span data-ttu-id="08a1c-107">Дополнительные сведения см. в разделе [Завершение работы](shutting-down.md).</span><span class="sxs-lookup"><span data-stu-id="08a1c-107">For more information, see [Shutting Down](shutting-down.md).</span></span> <span data-ttu-id="08a1c-108">Пример см. в разделе [Завершение работы системы](how-to-shut-down-the-system.md).</span><span class="sxs-lookup"><span data-stu-id="08a1c-108">For an example, see [How to Shut Down the System](how-to-shut-down-the-system.md).</span></span>

<span data-ttu-id="08a1c-109">При выходе из системы останавливаются все процессы, связанные с контекстом безопасности процесса, который вызвал функцию Exit, записывает текущего пользователя в систему и отображает диалоговое окно входа.</span><span class="sxs-lookup"><span data-stu-id="08a1c-109">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span> <span data-ttu-id="08a1c-110">Дополнительные сведения см. в разделе выход [из системы](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="08a1c-110">For more information, see [Logging Off](logging-off.md).</span></span> <span data-ttu-id="08a1c-111">Пример см. в разделе выход [из текущего пользователя](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="08a1c-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="08a1c-112">Блокировка рабочей станции защищает экран от несанкционированного использования при каждом выходе компьютера из системы.</span><span class="sxs-lookup"><span data-stu-id="08a1c-112">Locking the workstation protects the display from unauthorized use whenever you leave your computer.</span></span> <span data-ttu-id="08a1c-113">Чтобы разблокировать рабочую станцию, необходимо войти в систему.</span><span class="sxs-lookup"><span data-stu-id="08a1c-113">To unlock the workstation, you must log in.</span></span> <span data-ttu-id="08a1c-114">Пример см. в разделе [Блокировка рабочей станции](how-to-lock-the-workstation.md).</span><span class="sxs-lookup"><span data-stu-id="08a1c-114">For an example, see [How to Lock the Workstation](how-to-lock-the-workstation.md).</span></span>

<span data-ttu-id="08a1c-115">Средство [регистрации событий завершения работы](shutdown-event-tracker.md) позволяет пользователю или приложению документировать причину завершения работы или перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="08a1c-115">The [Shutdown Event Tracker](shutdown-event-tracker.md) enables the user or application to document the reason for shutting down or restarting the system.</span></span>

 

 



