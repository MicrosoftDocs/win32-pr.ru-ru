---
description: Сеансы трассировки событий записывают события от одного или нескольких поставщиков.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Управление сеансами трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984520"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="94a4e-103">Управление сеансами трассировки событий</span><span class="sxs-lookup"><span data-stu-id="94a4e-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="94a4e-104">Сеансы трассировки событий записывают события от одного или нескольких [поставщиков](providing-events.md).</span><span class="sxs-lookup"><span data-stu-id="94a4e-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="94a4e-105">Контроллер определяет сеанс и включает поставщиков.</span><span class="sxs-lookup"><span data-stu-id="94a4e-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="94a4e-106">Определение сеанса обычно включает в себя указание имени сеанса и файла журнала, тип используемого файла журнала и разрешение метки времени, используемой для записи событий.</span><span class="sxs-lookup"><span data-stu-id="94a4e-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="94a4e-107">Контроллеры также могут обновлять сеансы трассировки событий и запрашивать их.</span><span class="sxs-lookup"><span data-stu-id="94a4e-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="94a4e-108">В следующих разделах показано, как определить и обновить сеанс, а также включить поставщики трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="94a4e-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="94a4e-109">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="94a4e-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="94a4e-110">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="94a4e-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="94a4e-111">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="94a4e-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="94a4e-112">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="94a4e-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="94a4e-113">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="94a4e-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="94a4e-114">Извлечение дополнительных данных трассировки событий</span><span class="sxs-lookup"><span data-stu-id="94a4e-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="94a4e-115">Сведения о сбросе и запросе сеансов см. в разделе [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea) и [**куеряллтрацес**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa)соответственно.</span><span class="sxs-lookup"><span data-stu-id="94a4e-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="94a4e-116">Управлять сеансами трассировки событий могут только пользователи, работающие с повышенными правами администратора, пользователи из группы "Пользователи журналов производительности" и приложения, работающие в качестве LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="94a4e-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="94a4e-117">Чтобы предоставить ограниченному пользователю возможность управлять сеансами трассировки, добавьте их в группу "Пользователи журнала производительности".</span><span class="sxs-lookup"><span data-stu-id="94a4e-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="94a4e-118">**Windows XP и windows 2000:** Любой пользователь может управлять сеансом трассировки.</span><span class="sxs-lookup"><span data-stu-id="94a4e-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 
