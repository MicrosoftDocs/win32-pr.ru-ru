---
description: Когда функция обработчика вызывается потоком Dispatcher, она обрабатывает код элемента управления, переданный в параметре кода операции, а затем вызывает функцию Репортсвкстатус для обновления состояния службы.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Написание функции обработчика элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662345"
---
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="95e84-103">Написание функции обработчика элемента управления</span><span class="sxs-lookup"><span data-stu-id="95e84-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="95e84-104">Когда функция [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) вызывается потоком Dispatcher, она обрабатывает код элемента управления, переданный в параметре *кода операции* , а затем вызывает функцию репортсвкстатус для обновления состояния службы.</span><span class="sxs-lookup"><span data-stu-id="95e84-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="95e84-105">Когда функция [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) получает управляющий код, она должна сообщить о состоянии службы, только если обработка управляющего кода приводит к изменению состояния службы.</span><span class="sxs-lookup"><span data-stu-id="95e84-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="95e84-106">Если служба не работает на элементе управления, она не должна сообщать о состоянии диспетчеру управления службами.</span><span class="sxs-lookup"><span data-stu-id="95e84-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="95e84-107">Исходный код для Репортсвкстатус см. в разделе [написание функции ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="95e84-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="95e84-108">В следующем примере функция Свкктрлхандлер является примером функции [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) .</span><span class="sxs-lookup"><span data-stu-id="95e84-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="95e84-109">Обратите внимание, что переменная Гхсвкстопевент является глобальной переменной, которую следует инициализировать и использовать, как показано в [написании функции ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="95e84-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a><span data-ttu-id="95e84-110">См. также</span><span class="sxs-lookup"><span data-stu-id="95e84-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95e84-111">Функция обработчика управления службой</span><span class="sxs-lookup"><span data-stu-id="95e84-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="95e84-112">Полный пример службы</span><span class="sxs-lookup"><span data-stu-id="95e84-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



