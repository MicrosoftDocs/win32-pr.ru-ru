---
description: В следующем примере функция Екситвиндовс используется для выхода текущего пользователя из системы.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Выход из системы текущего пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998481"
---
# <a name="how-to-log-off-the-current-user"></a><span data-ttu-id="81e8c-103">Выход из системы текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="81e8c-103">How to Log Off the Current User</span></span>

<span data-ttu-id="81e8c-104">В следующем примере функция [**екситвиндовс**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) используется для выхода текущего пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="81e8c-104">The following example uses the [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

<span data-ttu-id="81e8c-105">В следующем примере функция [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) используется для выхода текущего пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="81e8c-105">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

<span data-ttu-id="81e8c-106">Приложение получает сообщение [**WM \_ куерендсессион**](wm-queryendsession.md) и отображает диалоговое окно с просьбой подтвердить завершение сеанса.</span><span class="sxs-lookup"><span data-stu-id="81e8c-106">The application receives the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message and displays a dialog box asking the whether it is OK to end the session.</span></span> <span data-ttu-id="81e8c-107">Если пользователь нажмет кнопку **Да**, система выполнит выход пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="81e8c-107">If the user clicks **Yes**, the system logs off the user.</span></span> <span data-ttu-id="81e8c-108">Если пользователь нажмет кнопку **нет**, выход из системы отменяется.</span><span class="sxs-lookup"><span data-stu-id="81e8c-108">If the user clicks **No**, the logoff is canceled.</span></span>

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a><span data-ttu-id="81e8c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="81e8c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81e8c-110">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="81e8c-110">Logging Off</span></span>](logging-off.md)
</dt> </dl>

 

 



