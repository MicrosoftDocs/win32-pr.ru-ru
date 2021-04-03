---
title: Очистка виртуального каталога
description: Служба BITS расширяет виртуальные каталоги IIS для поддержки отправки.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987678"
---
# <a name="virtual-directory-cleanup"></a><span data-ttu-id="82c04-103">Очистка виртуального каталога</span><span class="sxs-lookup"><span data-stu-id="82c04-103">Virtual Directory Cleanup</span></span>

<span data-ttu-id="82c04-104">Служба BITS расширяет виртуальные каталоги IIS для поддержки отправки.</span><span class="sxs-lookup"><span data-stu-id="82c04-104">BITS extends IIS virtual directories to support uploads.</span></span> <span data-ttu-id="82c04-105">У каждого виртуального каталога есть свойство времени ожидания сеанса (свойство метабазы IIS [битссессионтимеаут](bits-iis-extension-properties.md) ), которое указывает период времени, в течение которого клиент BITS должен выполнить загрузку файла.</span><span class="sxs-lookup"><span data-stu-id="82c04-105">Each virtual directory has a session time-out property (the IIS [BITSSessionTimeout](bits-iis-extension-properties.md) metabase property) that specifies the period of time in which the BITS client must make progress in uploading the file.</span></span> <span data-ttu-id="82c04-106">Если в течение этого периода времени не выполняется (таймер сбрасывается при выполнении), служба BITS закрывает сеанс.</span><span class="sxs-lookup"><span data-stu-id="82c04-106">If no progress is made during that period (the timer is reset when progress is made), BITS closes the session.</span></span> <span data-ttu-id="82c04-107">По умолчанию время ожидания сеанса составляет 14 дней.</span><span class="sxs-lookup"><span data-stu-id="82c04-107">The default session time-out is 14 days.</span></span>

<span data-ttu-id="82c04-108">Служба BITS добавляет рабочий элемент в [планировщик задач](/windows/desktop/TaskSchd/task-scheduler-start-page) для каждого создаваемого и включенного виртуального каталога.</span><span class="sxs-lookup"><span data-stu-id="82c04-108">BITS adds a work item to the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) for each virtual directory you create and enable.</span></span> <span data-ttu-id="82c04-109">Рабочий элемент удаляет ресурсы, связанные с закрытыми сеансами.</span><span class="sxs-lookup"><span data-stu-id="82c04-109">The work item deletes resources associated with the closed sessions.</span></span> <span data-ttu-id="82c04-110">По умолчанию очистка выполняется каждые 12 часов.</span><span class="sxs-lookup"><span data-stu-id="82c04-110">By default, the cleanup occurs every 12 hours.</span></span> <span data-ttu-id="82c04-111">Если два виртуальных каталога указывают на один и тот же физический каталог, процесс очистки, инициированный одним из каталогов, удаляет ресурсы, связанные со всеми закрытыми сеансами в физическом каталоге.</span><span class="sxs-lookup"><span data-stu-id="82c04-111">If two virtual directories point to the same physical directory, the cleanup process initiated by one of the directories deletes the resources associated with all closed sessions in the physical directory.</span></span>

<span data-ttu-id="82c04-112">Используйте вкладку расширение BITS или интерфейсы [планировщик задач](/windows/desktop/TaskSchd/task-scheduler-start-page) , чтобы изменить расписание очистки в соответствии с вашими приложениями.</span><span class="sxs-lookup"><span data-stu-id="82c04-112">Use the BITS Extension tab or the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) interfaces to change the cleanup schedule as appropriate for your application.</span></span> <span data-ttu-id="82c04-113">Можно также вызвать метод [**ибитсекстенсионсетуп:: жетклеануптаск**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) , чтобы получить указатель интерфейса на задачу очистки, связанную с виртуальным каталогом.</span><span class="sxs-lookup"><span data-stu-id="82c04-113">You can also call the [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) method to retrieve an interface pointer to the cleanup task associated with the virtual directory.</span></span>

> [!Note]  
> <span data-ttu-id="82c04-114">Если планировщик задач отключена после включения виртуального каталога, процесс очистки виртуального каталога не будет работать.</span><span class="sxs-lookup"><span data-stu-id="82c04-114">If the Task Scheduler is disabled after the virtual directory is enabled, the virtual directory cleanup process will not work.</span></span>

 

 

 