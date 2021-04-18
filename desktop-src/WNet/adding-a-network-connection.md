---
title: Добавление сетевого подключения
description: Чтобы установить соединение с сетевым ресурсом, описанным структурой НЕТРЕСАУРЦЕ, приложение может вызвать функцию WNetAddConnection2, WNetAddConnection3 или Внетусеконнектион.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710325"
---
# <a name="adding-a-network-connection"></a><span data-ttu-id="96322-103">Добавление сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="96322-103">Adding a Network Connection</span></span>

<span data-ttu-id="96322-104">Чтобы установить соединение с сетевым ресурсом, описанным структурой [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , приложение может вызвать функцию [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)или [**внетусеконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) .</span><span class="sxs-lookup"><span data-stu-id="96322-104">To make a connection to a network resource described by a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure, an application can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), or the [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) function.</span></span> <span data-ttu-id="96322-105">В следующем примере демонстрируется использование функции **WNetAddConnection2** .</span><span class="sxs-lookup"><span data-stu-id="96322-105">The following example demonstrates use of the **WNetAddConnection2** function.</span></span>

<span data-ttu-id="96322-106">В примере кода вызывается функция **WNetAddConnection2** , указывающая, что система должна обновить профиль пользователя с информацией, создав "сохраненное" или постоянное подключение.</span><span class="sxs-lookup"><span data-stu-id="96322-106">The code sample calls the **WNetAddConnection2** function, specifying that the system should update the user's profile with the information, creating a "remembered" or persistent connection.</span></span> <span data-ttu-id="96322-107">В примере вызывается определяемый приложением обработчик ошибок для обработки ошибок и функция [**текста**](/windows/desktop/api/wingdi/nf-wingdi-textouta) для печати.</span><span class="sxs-lookup"><span data-stu-id="96322-107">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



<span data-ttu-id="96322-108">Функция [**внетаддконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) поддерживается для совместимости с более ранними версиями Windows для рабочих групп.</span><span class="sxs-lookup"><span data-stu-id="96322-108">The [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="96322-109">Новые приложения должны вызывать функцию [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) или функцию [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .</span><span class="sxs-lookup"><span data-stu-id="96322-109">New applications should call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function.</span></span>

<span data-ttu-id="96322-110">Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="96322-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 