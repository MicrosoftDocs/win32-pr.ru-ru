---
description: В следующем примере Рабочая станция блокируется с помощью функции Локкворкстатион. Система отображает диалоговое окно Блокировка рабочей станции. В диалоговом окне появляется сообщение о том, что Рабочая станция используется и заблокирована пользователем.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Как заблокировать рабочую станцию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910331"
---
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="11853-105">Как заблокировать рабочую станцию</span><span class="sxs-lookup"><span data-stu-id="11853-105">How to Lock the Workstation</span></span>

<span data-ttu-id="11853-106">В следующем примере Рабочая станция блокируется с помощью функции [**локкворкстатион**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) .</span><span class="sxs-lookup"><span data-stu-id="11853-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="11853-107">Система отображает диалоговое окно **Блокировка рабочей станции** .</span><span class="sxs-lookup"><span data-stu-id="11853-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="11853-108">В диалоговом окне появляется сообщение о том, что Рабочая станция используется и заблокирована пользователем.</span><span class="sxs-lookup"><span data-stu-id="11853-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



<span data-ttu-id="11853-109">Чтобы определить, заблокирована ли Рабочая станция, проверьте, является ли окно видимым.</span><span class="sxs-lookup"><span data-stu-id="11853-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="11853-110">Рабочая станция может быть разблокирована пользователем или администратором.</span><span class="sxs-lookup"><span data-stu-id="11853-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="11853-111">Чтобы разблокировать систему, нажмите клавиши Ctrl + Alt + Del и войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="11853-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="11853-112">Чтобы получить уведомление при входе пользователя в систему, используйте функцию [**втсрегистерсессионнотификатион**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) , чтобы зарегистрироваться для получения сообщений об [**\_ \_ изменениях в WM втссессион**](../termserv/wm-wtssession-change.md) .</span><span class="sxs-lookup"><span data-stu-id="11853-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="11853-113">При получении этого сообщения проверьте, равен ли параметр *wParam* \_ блокировке сеанса ВТС \_ .</span><span class="sxs-lookup"><span data-stu-id="11853-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
