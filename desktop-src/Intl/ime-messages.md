---
description: Операционная система отправляет сообщения окна IME в процедуру окна приложения при возникновении определенных событий, влияющих на окна IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Сообщения IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072818"
---
# <a name="ime-messages"></a><span data-ttu-id="6d993-103">Сообщения IME</span><span class="sxs-lookup"><span data-stu-id="6d993-103">IME Messages</span></span>

<span data-ttu-id="6d993-104">Операционная система отправляет сообщения окна IME в процедуру окна приложения при возникновении определенных событий, влияющих на окна IME.</span><span class="sxs-lookup"><span data-stu-id="6d993-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="6d993-105">Например, операционная система отправляет в приложение сообщение [**\_ \_ SETCONTEXT редактора WM IME**](wm-ime-setcontext.md) при активации окна.</span><span class="sxs-lookup"><span data-stu-id="6d993-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="6d993-106">Приложения, не поддерживающие IME, передают эти сообщения функции [дефвиндовпрок](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , которая отправляет их в СООТВЕТСТВУЮЩЕЕ окно IME по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d993-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="6d993-107">Приложения, поддерживающие IME, либо обрабатывают эти сообщения, либо пересылают их в собственные окна IME.</span><span class="sxs-lookup"><span data-stu-id="6d993-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="6d993-108">Приложение может направлять окно IME для выполнения команды, например, изменять расположение окна композиции с помощью [**\_ \_ управляющего сообщения WM IME**](wm-ime-control.md) .</span><span class="sxs-lookup"><span data-stu-id="6d993-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="6d993-109">Редактор IME уведомляет приложение об изменениях в строке композиции с помощью сообщения о [**\_ \_ композиции редактора WM IME**](wm-ime-composition.md) , а также об общих изменениях состояния окон IME путем отправки сообщения [**\_ \_ уведомления WM IME**](wm-ime-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6d993-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d993-110">См. также</span><span class="sxs-lookup"><span data-stu-id="6d993-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d993-111">О диспетчере методов ввода</span><span class="sxs-lookup"><span data-stu-id="6d993-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
