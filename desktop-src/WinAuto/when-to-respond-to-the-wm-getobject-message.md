---
title: Когда следует отвечать на WM_GETOBJECT сообщение
description: Если приложение поддерживает Microsoft Active Accessibility или автоматизацию пользовательского интерфейса для элемента пользовательского интерфейса, приложение не должно отвечать на сообщение WM \_ GetObject, прежде чем объект, представляющий элемент пользовательского интерфейса, полностью инициализирован или после того, как приложение началось его закрытие.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488137"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a><span data-ttu-id="7a29a-103">Когда следует отвечать на сообщение WM \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="7a29a-103">When to Respond to the WM\_GETOBJECT Message</span></span>

<span data-ttu-id="7a29a-104">Если приложение поддерживает Microsoft Active Accessibility или автоматизацию пользовательского интерфейса для элемента пользовательского интерфейса, приложение не должно отвечать на сообщение [**WM \_ GetObject**](wm-getobject.md) , прежде чем объект, представляющий элемент пользовательского интерфейса, полностью инициализирован или после того, как приложение началось его закрытие.</span><span class="sxs-lookup"><span data-stu-id="7a29a-104">If an application supports Microsoft Active Accessibility or UI Automation for a UI element, the application must not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message before the object that represents the UI element is fully initialized, or after the application has begun to close.</span></span> <span data-ttu-id="7a29a-105">Когда приложение создает новое окно, система создает [**\_ объект события \_ CREATE**](event-constants.md) WinEvent для уведомления клиентов перед отправкой сообщения о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) в процедуру окна приложения.</span><span class="sxs-lookup"><span data-stu-id="7a29a-105">When an application creates a new window, the system raises the [**EVENT\_OBJECT\_CREATE**](event-constants.md) WinEvent to notify clients before sending the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to the application's window procedure.</span></span> <span data-ttu-id="7a29a-106">Поскольку многие приложения используют приложение **WM \_ CREATE** для запуска процесса инициализации, любая реализация элемента пользовательского интерфейса не реагирует на сообщение [**WM \_ GetObject**](wm-getobject.md) до тех пор, пока приложение не завершит обработку сообщения **WM \_ CREATE** .</span><span class="sxs-lookup"><span data-stu-id="7a29a-106">Because many applications use **WM\_CREATE** to start the initialization process, any accessibility implementation of a UI element does not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message until after the application has finished processing the **WM\_CREATE** message.</span></span>

 

 