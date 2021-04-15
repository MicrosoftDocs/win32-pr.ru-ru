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
# <a name="writing-a-control-handler-function"></a>Написание функции обработчика элемента управления

Когда функция [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) вызывается потоком Dispatcher, она обрабатывает код элемента управления, переданный в параметре *кода операции* , а затем вызывает функцию репортсвкстатус для обновления состояния службы. Когда функция [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) получает управляющий код, она должна сообщить о состоянии службы, только если обработка управляющего кода приводит к изменению состояния службы. Если служба не работает на элементе управления, она не должна сообщать о состоянии диспетчеру управления службами. Исходный код для Репортсвкстатус см. в разделе [написание функции ServiceMain](writing-a-servicemain-function.md).

В следующем примере функция Свкктрлхандлер является примером функции [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) . Обратите внимание, что переменная Гхсвкстопевент является глобальной переменной, которую следует инициализировать и использовать, как показано в [написании функции ServiceMain](writing-a-servicemain-function.md).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Функция обработчика управления службой](service-control-handler-function.md)
</dt> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 



