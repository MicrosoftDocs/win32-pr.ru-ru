---
title: Создание окна Авикап Capture
description: Создание окна Авикап Capture
ms.assetid: a1418e98-f16d-401a-94a7-64fb272a39e2
keywords:
- Функция Капкреатекаптуревиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d035d44b8d0b46df31afa5c3235e59286121c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329283"
---
# <a name="creating-an-avicap-capture-window"></a><span data-ttu-id="25843-104">Создание окна Авикап Capture</span><span class="sxs-lookup"><span data-stu-id="25843-104">Creating an AVICap Capture Window</span></span>

<span data-ttu-id="25843-105">Окно Capture класса Авикап Window можно создать с помощью функции [**капкреатекаптуревиндов**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .</span><span class="sxs-lookup"><span data-stu-id="25843-105">You can create a capture window of the AVICap window class by using the [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) function.</span></span> <span data-ttu-id="25843-106">Эта функция возвращает маркер окна, который определяет окно записи и используется приложением для отправки последующих сообщений в окно.</span><span class="sxs-lookup"><span data-stu-id="25843-106">This function returns a window handle that identifies the capture window and is used by an application to send subsequent messages to the window.</span></span>

<span data-ttu-id="25843-107">Можно создать одно или несколько окон захвата в приложении и подключить каждое окно захвата к другому устройству записи.</span><span class="sxs-lookup"><span data-stu-id="25843-107">You can create one or more capture windows in an application and connect each capture window to a different capture device.</span></span>

 

 




