---
description: Интерфейс поставщика поддержки безопасности (SSPI) позволяет приложению использовать различные модели безопасности, доступные на компьютере или в сети, не изменяя интерфейс системы безопасности.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Модель SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423621"
---
# <a name="sspi-model"></a><span data-ttu-id="7216a-103">Модель SSPI</span><span class="sxs-lookup"><span data-stu-id="7216a-103">SSPI Model</span></span>

<span data-ttu-id="7216a-104">[*Интерфейс поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI) позволяет приложению использовать различные модели безопасности, доступные на компьютере или в сети, не изменяя интерфейс системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7216a-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) allows an application to use various security models available on a computer or network without changing the interface to the security system.</span></span> <span data-ttu-id="7216a-105">SSPI не устанавливает [*учетные данные*](../secgloss/c-gly.md) для входа в систему, так как обычно это привилегированная операция, обрабатываемая операционной системой.</span><span class="sxs-lookup"><span data-stu-id="7216a-105">SSPI does not establish logon [*credentials*](../secgloss/c-gly.md) because that is generally a privileged operation handled by the operating system.</span></span>

<span data-ttu-id="7216a-106">[*Поставщик поддержки безопасности*](../secgloss/s-gly.md) (SSP) содержится в [*библиотеке динамической компоновки*](../secgloss/d-gly.md) (DLL), которая реализует SSPI, делая один или несколько [*пакетов безопасности*](../secgloss/s-gly.md) доступными для приложений.</span><span class="sxs-lookup"><span data-stu-id="7216a-106">A [*security support provider*](../secgloss/s-gly.md) (SSP) is contained in a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements SSPI by making one or more [*security packages*](../secgloss/s-gly.md) available to applications.</span></span> <span data-ttu-id="7216a-107">Каждый пакет безопасности предоставляет сопоставления между вызовами функции SSPI приложения и функциями реальной модели безопасности.</span><span class="sxs-lookup"><span data-stu-id="7216a-107">Each security package provides mappings between the SSPI function calls of an application and the functions of an actual security model.</span></span> <span data-ttu-id="7216a-108">Пакеты безопасности поддерживают такие [*протоколы безопасности*](../secgloss/s-gly.md) , как проверка подлинности [*Kerberos*](../secgloss/k-gly.md) и диспетчер LAN.</span><span class="sxs-lookup"><span data-stu-id="7216a-108">Security packages support [*security protocols*](../secgloss/s-gly.md) such as [*Kerberos*](../secgloss/k-gly.md) authentication and LAN Manager.</span></span>

<span data-ttu-id="7216a-109">Интерфейс SSPI доступен в режиме ядра, а также в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="7216a-109">The SSPI interface is available in kernel mode as well as user mode.</span></span> <span data-ttu-id="7216a-110">Чтобы использовать функциональность SSPI в режиме ядра, необходимо установить набор DDK по установке файловой системы Windows.</span><span class="sxs-lookup"><span data-stu-id="7216a-110">To use SSPI functionality in kernel mode, you must install the Windows Installable File System DDK.</span></span> <span data-ttu-id="7216a-111">Вызывающая модель остается неизменной, но рекомендации режима ядра указаны на страницах справки по функциям.</span><span class="sxs-lookup"><span data-stu-id="7216a-111">The calling model remains the same, but kernel mode considerations are noted on function reference pages.</span></span> <span data-ttu-id="7216a-112">Дополнительные сведения см. в разделе [функции SSPI](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7216a-112">For more information, see [SSPI Functions](authentication-functions.md).</span></span>

 

 
