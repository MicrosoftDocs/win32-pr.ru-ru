---
description: Сведения о пакетах уведомлений Winlogon хранятся в реестре. В записях реестра указывается имя пакета уведомлений, имя библиотеки DLL, в которой реализован пакет, и имена функций, которые обрабатывали события Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Регистрация пакета уведомлений Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264359"
---
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="d2782-104">Регистрация пакета уведомлений Winlogon</span><span class="sxs-lookup"><span data-stu-id="d2782-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="d2782-105">Сведения о пакетах уведомлений [*Winlogon*](../secgloss/w-gly.md) хранятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="d2782-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="d2782-106">В записях реестра указывается имя пакета уведомлений, имя библиотеки DLL, в которой реализован пакет, и имена функций, которые обрабатывали события Winlogon.</span><span class="sxs-lookup"><span data-stu-id="d2782-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="d2782-107">При запуске Winlogon проверяет реестр и загружает все зарегистрированные пакеты уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d2782-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="d2782-108">При возникновении события Winlogon вызывает назначенную функцию обработчика событий для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="d2782-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="d2782-109">В системе могут быть зарегистрированы несколько пакетов уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="d2782-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="d2782-110">Чтобы зарегистрировать пакет уведомлений, создайте раздел реестра с именем **Notify** в качестве подраздела следующего раздела реестра и добавьте значения, описанные в [записях реестра](registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="d2782-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="d2782-111">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="d2782-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 
