---
description: Для пользователя преимущество многозадачности заключается в возможности одновременного открытия и работы нескольких приложений. Например, пользователь может редактировать файл с одним приложением, в то время как другое приложение пересчитывает электронную таблицу.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Преимущества многозадачности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673782"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="7dfb0-104">Преимущества многозадачности</span><span class="sxs-lookup"><span data-stu-id="7dfb0-104">Advantages of Multitasking</span></span>

<span data-ttu-id="7dfb0-105">Для пользователя преимущество многозадачности заключается в возможности одновременного открытия и работы нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="7dfb0-106">Например, пользователь может редактировать файл с одним приложением, в то время как другое приложение пересчитывает электронную таблицу.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="7dfb0-107">Для разработчиков приложений преимущество многозадачности заключается в возможности создания приложений, использующих более одного процесса, и создания процессов, использующих более одного потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="7dfb0-108">Например, процесс может иметь поток пользовательского интерфейса, который управляет взаимодействием с пользователем (ввод с клавиатуры и мышью), а также рабочими потоками, выполняющими другие задачи, в то время как поток пользовательского интерфейса ожидает ввода данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="7dfb0-109">Если присвоить потоку пользовательского интерфейса более высокий приоритет, приложение будет быстрее реагировать на него, тогда как рабочие потоки будут эффективно использовать процессор в течение времени, когда нет вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 



