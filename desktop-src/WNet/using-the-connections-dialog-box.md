---
title: Использование диалогового окна «соединения»
description: Функция Внетконнектиондиалог создает диалоговое окно, позволяющее пользователю просматривать сетевые ресурсы и подключаться к ним.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338204"
---
# <a name="using-the-connections-dialog-box"></a><span data-ttu-id="5b231-103">Использование диалогового окна «соединения»</span><span class="sxs-lookup"><span data-stu-id="5b231-103">Using the Connections Dialog Box</span></span>

<span data-ttu-id="5b231-104">Функция [**внетконнектиондиалог**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) создает диалоговое окно, позволяющее пользователю просматривать сетевые ресурсы и подключаться к ним.</span><span class="sxs-lookup"><span data-stu-id="5b231-104">The [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) function creates a dialog box that allows the user to browse and connect to network resources.</span></span> <span data-ttu-id="5b231-105">Вы также можете вызвать функцию [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) , чтобы создать диалоговое окно "соединения".</span><span class="sxs-lookup"><span data-stu-id="5b231-105">You can also call the [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) function to create a connections dialog box.</span></span> <span data-ttu-id="5b231-106">Для **WNetConnectionDialog1** требуется структура [**коннектдлгструкт**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .</span><span class="sxs-lookup"><span data-stu-id="5b231-106">**WNetConnectionDialog1** requires a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>

<span data-ttu-id="5b231-107">Функция [**внетдисконнектдиалог**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) создает диалоговое окно, позволяющее пользователю отключиться от сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b231-107">The [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) function creates a dialog box that allows the user to disconnect from network resources.</span></span>

<span data-ttu-id="5b231-108">В следующем примере кода показано, как вызвать функцию **внетконнектиондиалог** для создания диалогового окна, отображающего дисковые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5b231-108">The following code sample demonstrates how to call the **WNetConnectionDialog** function to create a dialog box that displays disk resources.</span></span> <span data-ttu-id="5b231-109">Если вызов завершается неудачей, пример вызывает обработчик ошибок, определенный приложением.</span><span class="sxs-lookup"><span data-stu-id="5b231-109">If the call fails, the sample calls an application-defined error handler.</span></span>


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



<span data-ttu-id="5b231-110">Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5b231-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 