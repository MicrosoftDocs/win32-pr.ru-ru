---
description: Чтобы уведомить пользователя о том, что возникла какая-либо ошибка, многие приложения просто создают звук с помощью функции Мессажебип или Flash-окна, используя функцию FlashWindow интерфейса или Флашвиндовекс.
ms.assetid: 35b6e93c-323a-4592-9394-a2e9dd79d9e6
title: Уведомление пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01a4e68b0c5dffcc5dcae5f2fe3b0c84288f59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262524"
---
# <a name="notifying-the-user"></a><span data-ttu-id="b6cc2-103">Уведомление пользователя</span><span class="sxs-lookup"><span data-stu-id="b6cc2-103">Notifying the User</span></span>

<span data-ttu-id="b6cc2-104">Чтобы уведомить пользователя о том, что возникла какая-либо ошибка, многие приложения просто создают звук с помощью функции [**мессажебип**](/windows/desktop/api/WinUser/nf-winuser-messagebeep) или Flash-окна, используя функцию [**FlashWindow интерфейса**](/windows/desktop/api/Winuser/nf-winuser-flashwindow) или [**флашвиндовекс**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex) .</span><span class="sxs-lookup"><span data-stu-id="b6cc2-104">To notify the user that some kind of error has occurred, many applications simply produce a sound by using the [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep) function or flash the window by using either the [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow) or [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex) function.</span></span> <span data-ttu-id="b6cc2-105">Приложение также может использовать эти функции, чтобы привлечь внимание к ошибке, а затем отобразить окно сообщения или сообщение об ошибке, содержащее сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b6cc2-105">An application can also use these functions to call attention to an error and then display a message box or an error message containing details about the error.</span></span>

 

 



