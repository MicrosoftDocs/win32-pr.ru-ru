---
description: Приложение делится на две программы. Одна из программ запускается от имени обычного пользователя, а другая запускается с правами администратора.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Модель брокера администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910616"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="e3d81-104">Модель брокера администратора</span><span class="sxs-lookup"><span data-stu-id="e3d81-104">Administrator Broker Model</span></span>

<span data-ttu-id="e3d81-105">В модели брокера администратора приложение делится на две программы.</span><span class="sxs-lookup"><span data-stu-id="e3d81-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="e3d81-106">Одна из программ запускается от имени обычного пользователя, а другая запускается с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="e3d81-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="e3d81-107">С помощью манифеста приложения пометьте стандартную пользовательскую программу **RequestedExecutionLevel** **asInvoker** и пометьте административную программу на **requestedExecutionLevel** **requireAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="e3d81-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="e3d81-108">Сначала пользователь запускает стандартную пользовательскую программу.</span><span class="sxs-lookup"><span data-stu-id="e3d81-108">A user launches the standard user program first.</span></span> <span data-ttu-id="e3d81-109">Когда пользователь пытается выполнить операцию, для которой требуется полный маркер доступа администратора, Стандартная пользовательская программа вызывает функцию [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) для запуска программы администрирования.</span><span class="sxs-lookup"><span data-stu-id="e3d81-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="e3d81-110">Функция **ShellExecute** запрашивает у пользователя утверждение перед запуском приложения с полным маркером доступа администратора пользователя.</span><span class="sxs-lookup"><span data-stu-id="e3d81-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="e3d81-111">Программа администрирования может выполнять задачи, требующие прав администратора.</span><span class="sxs-lookup"><span data-stu-id="e3d81-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="e3d81-112">Административная программа не полностью изолирована от стандартной пользовательской программы.</span><span class="sxs-lookup"><span data-stu-id="e3d81-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="e3d81-113">Административная программа может включить взаимодействие между процессами с помощью стандартной программы пользователя.</span><span class="sxs-lookup"><span data-stu-id="e3d81-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="e3d81-114">Однако такое взаимодействие ограничивается обязательной политикой целостности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3d81-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="e3d81-115">Сведения о обязательных особенностях целостности см. в разделе [Разработка приложений для запуска с низким уровнем целостности](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="e3d81-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="e3d81-116">Ниже приведены возможные варианты использования модели брокера администратора.</span><span class="sxs-lookup"><span data-stu-id="e3d81-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="e3d81-117">Разработка мастеров.</span><span class="sxs-lookup"><span data-stu-id="e3d81-117">Developing wizards.</span></span> <span data-ttu-id="e3d81-118">Если мастер оборудования определит, что необходимый драйвер не установлен на компьютере или расположен в утвержденном расположении предприятия, он вызывает приложение с повышенными правами, позволяющее переместить драйвер в хранилище компьютера.</span><span class="sxs-lookup"><span data-stu-id="e3d81-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="e3d81-119">Autorun.exe вызова Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="e3d81-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="e3d81-120">Когда пользователь запускает программное обеспечение с компакт-диска, Autorun.exe, который запускается от имени обычного пользователя, запускает Setup.exe, который запускается от имени администратора, для установки программного обеспечения на компьютер.</span><span class="sxs-lookup"><span data-stu-id="e3d81-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="e3d81-121">Ниже перечислены недостатки использования модели брокера администратора.</span><span class="sxs-lookup"><span data-stu-id="e3d81-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="e3d81-122">Переход от приложения к приложению может быть непонятен пользователю.</span><span class="sxs-lookup"><span data-stu-id="e3d81-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="e3d81-123">Сообщить пользователю о том, почему на мониторе появляется новое приложение, может быть трудно.</span><span class="sxs-lookup"><span data-stu-id="e3d81-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="e3d81-124">Передача сведений о состоянии между двумя приложениями может быть затруднена.</span><span class="sxs-lookup"><span data-stu-id="e3d81-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="e3d81-125">Например, эта модель не будет использоваться для передачи сведений о состоянии между стандартной панелью управления (CPL) и ее аналогом администратора просто для того, чтобы позволить тому же CPL использовать функции администрирования и обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="e3d81-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="e3d81-126">Стандартная пользовательская CPL должна хранить свое состояние в каком-то месте.</span><span class="sxs-lookup"><span data-stu-id="e3d81-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="e3d81-127">При разделении функциональных возможностей между двумя программами может быть много реплицируемого кода.</span><span class="sxs-lookup"><span data-stu-id="e3d81-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3d81-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e3d81-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d81-129">Разработка приложений, требующих прав администратора</span><span class="sxs-lookup"><span data-stu-id="e3d81-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="e3d81-130">Модель COM-объектов администратора</span><span class="sxs-lookup"><span data-stu-id="e3d81-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="e3d81-131">Модель службы операционной системы</span><span class="sxs-lookup"><span data-stu-id="e3d81-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="e3d81-132">Модель задач с повышенными правами</span><span class="sxs-lookup"><span data-stu-id="e3d81-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
