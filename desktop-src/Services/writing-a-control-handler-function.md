---
description: Когда функция обработчика вызывается потоком Dispatcher, она обрабатывает код элемента управления, переданный в параметре кода операции, а затем вызывает функцию Репортсвкстатус для обновления состояния службы.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Написание функции обработчика элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bf8ab32edb73fdf11f3f0370a512b17b143b8af219a2bd539e59bdf062a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888065"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функция обработчика управления службой](service-control-handler-function.md)
</dt> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 



