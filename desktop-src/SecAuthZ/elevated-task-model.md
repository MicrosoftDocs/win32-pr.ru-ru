---
description: Приложение, выполняющееся в качестве обычного пользователя, выполняет операции, требующие прав администратора, запуская запланированную задачу.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Модель задач с повышенными правами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348932"
---
# <a name="elevated-task-model"></a><span data-ttu-id="09a8c-103">Модель задач с повышенными правами</span><span class="sxs-lookup"><span data-stu-id="09a8c-103">Elevated Task Model</span></span>

<span data-ttu-id="09a8c-104">В модели задач с повышенными привилегиями приложение, выполняющееся в качестве обычного пользователя, выполняет операции, требующие прав администратора, запуская запланированную задачу.</span><span class="sxs-lookup"><span data-stu-id="09a8c-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="09a8c-105">**Windows Server 2003 и Windows XP:** Модель задач с повышенными правами не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09a8c-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="09a8c-106">Задачи не потребляют столько системных ресурсов, сколько служб, а задачи автоматически закрываются по завершении.</span><span class="sxs-lookup"><span data-stu-id="09a8c-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="09a8c-107">Рекомендуется использовать эту модель вместо [модели службы операционной системы](operating-system-service-model.md) , если не требуется обратная совместимость с операционными системами более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="09a8c-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="09a8c-108">Чтобы использовать задачу для выполнения привилегированных операций для стандартного пользовательского приложения, должны выполняться следующие условия.</span><span class="sxs-lookup"><span data-stu-id="09a8c-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="09a8c-109">Задача должна быть настроена для запуска от имени **System**.</span><span class="sxs-lookup"><span data-stu-id="09a8c-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="09a8c-110">[*Дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) , связанный с задачей, должен быть настроен таким, чтобы позволить обычным пользователям запускать задачу.</span><span class="sxs-lookup"><span data-stu-id="09a8c-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="09a8c-111">Должна быть запущена служба планировщика заданий.</span><span class="sxs-lookup"><span data-stu-id="09a8c-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="09a8c-112">Сведения о создании и запуске задач см. в разделе [планировщик задач](/windows/desktop/TaskSchd/task-scheduler-start-page).</span><span class="sxs-lookup"><span data-stu-id="09a8c-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09a8c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="09a8c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a8c-114">Разработка приложений, требующих прав администратора</span><span class="sxs-lookup"><span data-stu-id="09a8c-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="09a8c-115">Модель брокера администратора</span><span class="sxs-lookup"><span data-stu-id="09a8c-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="09a8c-116">Модель COM-объектов администратора</span><span class="sxs-lookup"><span data-stu-id="09a8c-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="09a8c-117">Модель службы операционной системы</span><span class="sxs-lookup"><span data-stu-id="09a8c-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
