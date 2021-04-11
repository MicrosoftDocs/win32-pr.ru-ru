---
description: При завершении работы системы используются следующие функции.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Функции завершения работы системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998616"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="44703-103">Функции завершения работы системы</span><span class="sxs-lookup"><span data-stu-id="44703-103">System Shutdown Functions</span></span>

<span data-ttu-id="44703-104">При завершении работы системы используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="44703-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="44703-105">Функция</span><span class="sxs-lookup"><span data-stu-id="44703-105">Function</span></span>                                                         | <span data-ttu-id="44703-106">Описание</span><span class="sxs-lookup"><span data-stu-id="44703-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44703-107">**абортсистемшутдовн**</span><span class="sxs-lookup"><span data-stu-id="44703-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="44703-108">Останавливает запущенное завершение работы системы.</span><span class="sxs-lookup"><span data-stu-id="44703-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="44703-109">**екситвиндовс**</span><span class="sxs-lookup"><span data-stu-id="44703-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="44703-110">Выполнит выход интерактивного пользователя.</span><span class="sxs-lookup"><span data-stu-id="44703-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="44703-111">**Функцию**</span><span class="sxs-lookup"><span data-stu-id="44703-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="44703-112">Выполнит выход интерактивного пользователя, завершит работу системы или завершит работу и перезапустит систему.</span><span class="sxs-lookup"><span data-stu-id="44703-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="44703-113">**инитиатешутдовн**</span><span class="sxs-lookup"><span data-stu-id="44703-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="44703-114">Инициирует завершение работы и перезагрузку указанного компьютера и перезапускает все приложения, зарегистрированные для перезапуска.</span><span class="sxs-lookup"><span data-stu-id="44703-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="44703-115">**инитиатесистемшутдовн**</span><span class="sxs-lookup"><span data-stu-id="44703-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="44703-116">Инициирует завершение работы и необязательное перезагрузку указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="44703-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="44703-117">**инитиатесистемшутдовнекс**</span><span class="sxs-lookup"><span data-stu-id="44703-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="44703-118">Инициирует завершение работы и необязательное перезагрузку указанного компьютера и при необходимости записывает причину завершения работы.</span><span class="sxs-lookup"><span data-stu-id="44703-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="44703-119">**локкворкстатион**</span><span class="sxs-lookup"><span data-stu-id="44703-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="44703-120">Блокирует отображение рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="44703-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="44703-121">**шутдовнблоккреасонкреате**</span><span class="sxs-lookup"><span data-stu-id="44703-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="44703-122">Указывает, что система не может быть выключена, и задает строку причины, которая будет отображаться пользователю при инициировании выключения системы.</span><span class="sxs-lookup"><span data-stu-id="44703-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="44703-123">**шутдовнблоккреасондестрой**</span><span class="sxs-lookup"><span data-stu-id="44703-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="44703-124">Указывает, что система может завершить работу и освободить строку причины.</span><span class="sxs-lookup"><span data-stu-id="44703-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="44703-125">**шутдовнблоккреасонкуери**</span><span class="sxs-lookup"><span data-stu-id="44703-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="44703-126">Извлекает строку причины, заданную функцией [**шутдовнблоккреасонкреате**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="44703-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 



