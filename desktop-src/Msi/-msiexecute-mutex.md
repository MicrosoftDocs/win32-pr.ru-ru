---
description: '\_Мьютекс мсиексекуте задается только при обработке таблицы инсталлексекутесекуенце, таблицы админексекутесекуенце или таблицы адвтексекутесекуенце.'
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute мьютекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909172"
---
# <a name="_msiexecute-mutex"></a><span data-ttu-id="277b9-103">\_Мьютекс Мсиексекуте</span><span class="sxs-lookup"><span data-stu-id="277b9-103">\_MSIExecute Mutex</span></span>

<span data-ttu-id="277b9-104">\_Мьютекс мсиексекуте задается только при обработке [таблицы инсталлексекутесекуенце](installexecutesequence-table.md), таблицы [админексекутесекуенце](adminexecutesequence-table.md)или таблицы [адвтексекутесекуенце](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="277b9-104">The \_MSIExecute Mutex is set only while processing the [InstallExecuteSequence table](installexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

<span data-ttu-id="277b9-105">Поскольку две установки не могут быть запущены в одном процессе, попытка вызова программного интерфейса (API) установщика возвращает сообщение об ошибке \_ Installed \_ \_ (1618) в двух случаях:</span><span class="sxs-lookup"><span data-stu-id="277b9-105">Because two installations cannot be run in the same process, an attempt to call the installer's application programming interface (API) returns ERROR\_INSTALL\_ALREADY\_RUNNING (1618) in two cases:</span></span>

-   <span data-ttu-id="277b9-106">Пока \_ задан мьютекс мсиексекуте.</span><span class="sxs-lookup"><span data-stu-id="277b9-106">While the \_MSIExecute Mutex is set.</span></span>
-   <span data-ttu-id="277b9-107">Пока текущий процесс обрабатывает [таблицу инсталлуисекуенце](installuisequence-table.md) или [таблицу админуисекуенце](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="277b9-107">While the current process is processing the [InstallUISequence table](installuisequence-table.md) or [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="277b9-108">Сведения о том, какое приложение устанавливается, см. в сообщениях [журнала событий](event-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="277b9-108">See the [Event Logging](event-logging.md) messages for information about what application is being installed.</span></span>

<span data-ttu-id="277b9-109">В случаях, когда нецелесообразно возвращать ошибку \_ установки \_ , которая уже \_ выполнялась, можно получить текущее состояние службы установщик Windows, прежде чем пытаться начать установку с помощью функции [**куерисервицестатусекс**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) .</span><span class="sxs-lookup"><span data-stu-id="277b9-109">In cases where it is impractical to return an ERROR\_INSTALL\_ALREADY\_RUNNING error, you can retrieve the current status of the Windows Installer service before attempting to start the installation by using the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function.</span></span> <span data-ttu-id="277b9-110">Служба установщик Windows выполняется в данный момент, если значение элемента **двконтролсакцептед** в возвращаемой структуре [**\_ \_ процесса состояния службы**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) — это **\_ \_ Завершение работы службы Accept**.</span><span class="sxs-lookup"><span data-stu-id="277b9-110">The Windows Installer service is currently running if the value of the **dwControlsAccepted** member of the returned [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) structure is **SERVICE\_ACCEPT\_SHUTDOWN**.</span></span>

<span data-ttu-id="277b9-111">**Установщик Windows 2,0:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="277b9-111">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="277b9-112">Использование функции [**куерисервицестатусекс**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) для получения текущего состояния службы установщик Windows требует установщик Windows версии 3,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="277b9-112">The use of the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function to retrieve the current status of the Windows Installer service requires Windows Installer version 3.0 or greater.</span></span>

 

 
