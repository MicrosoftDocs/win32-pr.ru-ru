---
title: Интерфейсы КМГР
description: Используйте следующие интерфейсы диспетчера очередей (КМГР) для загрузки файлов и отслеживания заданий в очереди загрузки.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252815"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="244a1-103">Интерфейсы КМГР</span><span class="sxs-lookup"><span data-stu-id="244a1-103">QMGR Interfaces</span></span>

<span data-ttu-id="244a1-104">\[Интерфейсы диспетчера очереди (КМГР) доступны для использования в операционных системах, указанных в разделе требования раздела.</span><span class="sxs-lookup"><span data-stu-id="244a1-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="244a1-105">В последующих версиях они могут быть изменены или недоступны.</span><span class="sxs-lookup"><span data-stu-id="244a1-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="244a1-106">Вместо этого используйте [интерфейсы BITS](bits-interfaces.md).\]</span><span class="sxs-lookup"><span data-stu-id="244a1-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="244a1-107">Используйте следующие интерфейсы диспетчера очередей (КМГР) для загрузки файлов и отслеживания заданий в очереди загрузки.</span><span class="sxs-lookup"><span data-stu-id="244a1-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="244a1-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="244a1-108">Interface</span></span>                                                                 | <span data-ttu-id="244a1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="244a1-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="244a1-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="244a1-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="244a1-111">Реализуйте, чтобы получить уведомление при возникновении событий.</span><span class="sxs-lookup"><span data-stu-id="244a1-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="244a1-112">**ибаккграундкопиграуп**</span><span class="sxs-lookup"><span data-stu-id="244a1-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="244a1-113">Используйте для управления группой.</span><span class="sxs-lookup"><span data-stu-id="244a1-113">Use to manage the group.</span></span> <span data-ttu-id="244a1-114">Например, добавьте в группу задание, задайте свойства группы, а затем запустите и прервите группу в очереди загрузки.</span><span class="sxs-lookup"><span data-stu-id="244a1-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="244a1-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="244a1-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="244a1-116">Используйте для добавления файлов в задание и получения состояния задания.</span><span class="sxs-lookup"><span data-stu-id="244a1-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="244a1-117">**ибаккграундкопикмгр**</span><span class="sxs-lookup"><span data-stu-id="244a1-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="244a1-118">Используйте для создания новой группы, получения существующей группы или перечисления всех групп в очереди.</span><span class="sxs-lookup"><span data-stu-id="244a1-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="244a1-119">**иенумбаккграундкопиграупс**</span><span class="sxs-lookup"><span data-stu-id="244a1-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="244a1-120">Используйте для получения списка групп в очереди загрузки.</span><span class="sxs-lookup"><span data-stu-id="244a1-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="244a1-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="244a1-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="244a1-122">Используйте для получения списка заданий в группе.</span><span class="sxs-lookup"><span data-stu-id="244a1-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





