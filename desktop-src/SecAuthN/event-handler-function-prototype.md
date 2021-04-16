---
description: Функции прототипа обработчика событий используются для всех функций, которые обрабатывают события уведомлений Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Функция обратного вызова прототипа функции обработчика событий
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651103"
---
# <a name="event-handler-function-prototype-callback-function"></a>Функция обратного вызова прототипа функции обработчика событий

\[Функции прототипа обработчика событий больше не доступны для использования в Windows Server 2008 и Windows Vista. \]

Функции прототипа обработчика событий используются для всех функций, которые обрабатывают события уведомлений [*Winlogon*](/windows/desktop/SecGloss/w-gly) . Имя функции, представленное ниже *\_ \_ \_ имени функции обработчика событий* заполнителя, обычно отражает имя события, обрабатываемого функцией. Например, функция, обрабатывающая события входа в систему, может называться: **влевентлогон**.

## <a name="syntax"></a>Синтаксис


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ \_ сведений об уведомлении влкс**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) , которая содержит подробные сведения о событии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция обратного вызова не возвращает значение.

## <a name="remarks"></a>Комментарии

Если обработчику событий необходимо создать дочерние процессы, он должен вызвать функцию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . В противном случае новый процесс будет создан на рабочем столе Winlogon, а не на рабочем столе пользователя.

## <a name="examples"></a>Примеры

В следующем примере показано, как реализовать обработчики событий для событий Winlogon. Для простоты отображаются только реализации обработчиков событий входа и выхода из системы. Обработчики для остальных событий можно реализовать точно таким же образом.


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



 

