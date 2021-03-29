---
description: Для отладки службы можно использовать один из следующих методов.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Debugging a Service (Отладка службы)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809250"
---
# <a name="debugging-a-service"></a><span data-ttu-id="dbf36-103">Debugging a Service (Отладка службы)</span><span class="sxs-lookup"><span data-stu-id="dbf36-103">Debugging a Service</span></span>

<span data-ttu-id="dbf36-104">Для отладки службы можно использовать один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="dbf36-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="dbf36-105">Используйте отладчик для отладки службы во время ее работы.</span><span class="sxs-lookup"><span data-stu-id="dbf36-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="dbf36-106">Сначала получите идентификатор процесса (PID) процесса службы.</span><span class="sxs-lookup"><span data-stu-id="dbf36-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="dbf36-107">После получения идентификатора процесса присоединитесь к выполняющемуся процессу.</span><span class="sxs-lookup"><span data-stu-id="dbf36-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="dbf36-108">Сведения о синтаксисе см. в документации, прилагаемой к отладчику.</span><span class="sxs-lookup"><span data-stu-id="dbf36-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="dbf36-109">Вызовите функцию [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) , чтобы вызвать отладчик для JIT-отладки.</span><span class="sxs-lookup"><span data-stu-id="dbf36-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="dbf36-110">Укажите отладчик, который будет использоваться при запуске программы.</span><span class="sxs-lookup"><span data-stu-id="dbf36-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="dbf36-111">Для этого создайте ключ, называемый **выполнением файла изображения** , в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="dbf36-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="dbf36-112">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="dbf36-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="dbf36-113">Создайте подраздел с тем же именем, что и у службы (например, MYSERV.EXE).</span><span class="sxs-lookup"><span data-stu-id="dbf36-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="dbf36-114">В этот подраздел добавьте значение типа **reg \_ SZ** с именем **Debugger**.</span><span class="sxs-lookup"><span data-stu-id="dbf36-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="dbf36-115">Используйте полный путь к отладчику в качестве строкового значения.</span><span class="sxs-lookup"><span data-stu-id="dbf36-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="dbf36-116">В приложении панели управления "службы" выберите службу, нажмите кнопку " **Запуск** " и установите флажок " **разрешить службе взаимодействовать с рабочим столом**".</span><span class="sxs-lookup"><span data-stu-id="dbf36-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="dbf36-117">Служба должна быть интерактивной службой, иначе отладчик не сможет работать на рабочем столе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dbf36-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="dbf36-118">Обратите внимание, что этот метод больше не поддерживается в Windows Vista, поскольку все службы выполняются в сеансе, который зарезервирован исключительно для служб и не поддерживает отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dbf36-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="dbf36-119">Используйте [трассировку событий](/windows/desktop/ETW/event-tracing-portal) для записи данных в журнал.</span><span class="sxs-lookup"><span data-stu-id="dbf36-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="dbf36-120">Для отладки кода инициализации службы автозапуска необходимо временно установить и запустить службу в качестве службы запуска по требованию.</span><span class="sxs-lookup"><span data-stu-id="dbf36-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="dbf36-121">Иногда может потребоваться запустить службу в качестве консольного приложения для отладки.</span><span class="sxs-lookup"><span data-stu-id="dbf36-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="dbf36-122">В этом сценарии функция [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) будет возвращать **ошибку \_ Failed \_ Service \_ Controller \_ Connect**.</span><span class="sxs-lookup"><span data-stu-id="dbf36-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="dbf36-123">Поэтому не забудьте структурировать код таким образом, чтобы код, зависящий от службы, не вызывался при возвращении этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="dbf36-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbf36-124">См. также</span><span class="sxs-lookup"><span data-stu-id="dbf36-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf36-125">Отладка приложения службы</span><span class="sxs-lookup"><span data-stu-id="dbf36-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="dbf36-126">Средства отладки для Windows</span><span class="sxs-lookup"><span data-stu-id="dbf36-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
