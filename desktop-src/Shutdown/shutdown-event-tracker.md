---
description: Средство регистрации событий завершения работы позволяет пользователю или приложению документировать причину завершения работы или перезапуска системы.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Средство регистрации событий завершения работы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345705"
---
# <a name="shutdown-event-tracker"></a><span data-ttu-id="6f74c-103">Средство регистрации событий завершения работы</span><span class="sxs-lookup"><span data-stu-id="6f74c-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="6f74c-104">Средство *регистрации событий завершения работы* позволяет пользователю или приложению документировать причину завершения работы или перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="6f74c-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="6f74c-105">Пользователю предлагается ввести сведения при выборе команды **Завершение работы** в меню " **Пуск** " или при использовании Shutdown.exe.</span><span class="sxs-lookup"><span data-stu-id="6f74c-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="6f74c-106">Разработчики могут включать код причины при вызове функций [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) и [**инитиатесистемшутдовнекс**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .</span><span class="sxs-lookup"><span data-stu-id="6f74c-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="6f74c-107">Информация хранится в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="6f74c-107">The information is stored in the event log.</span></span>

<span data-ttu-id="6f74c-108">**Windows XP:** Хотя эта функция включена по умолчанию начиная с Windows Server 2003, ее необходимо включить в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6f74c-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="6f74c-109">Дополнительные сведения см. в документации по средству регистрации событий завершения работы, включенному в систему или на сайте TechNet.</span><span class="sxs-lookup"><span data-stu-id="6f74c-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="6f74c-110">Функции [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) и [**инитиатесистемшутдовнекс**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) были обновлены для поддержки кодов причин завершения работы в параметре *параметр dwReason* .</span><span class="sxs-lookup"><span data-stu-id="6f74c-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="6f74c-111">Используйте значения, определенные в поле Reason. h для создания кода причины завершения работы, или определите пользовательский код причины.</span><span class="sxs-lookup"><span data-stu-id="6f74c-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="6f74c-112">Код причины завершения работы создается на основе основного флага, дополнительного флага и двух необязательных флагов.</span><span class="sxs-lookup"><span data-stu-id="6f74c-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="6f74c-113">Дополнительные сведения см. в разделе [коды причин завершения работы системы](system-shutdown-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6f74c-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f74c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6f74c-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f74c-115">[Средство регистрации событий завершения работы (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6f74c-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
