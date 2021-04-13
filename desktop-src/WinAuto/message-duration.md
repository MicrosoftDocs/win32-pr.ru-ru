---
title: Параметр длительности сообщения
description: Приложения обычно используют всплывающие окна для краткого отображения важных сообщений уведомления пользователю. Приложение создает окно, отображает его для определенной в приложении длительности, а затем уничтожает окно.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413088"
---
# <a name="message-duration-parameter"></a><span data-ttu-id="fd371-104">Параметр длительности сообщения</span><span class="sxs-lookup"><span data-stu-id="fd371-104">Message duration parameter</span></span>

<span data-ttu-id="fd371-105">Приложения обычно используют всплывающие окна для краткого отображения важных сообщений уведомления пользователю.</span><span class="sxs-lookup"><span data-stu-id="fd371-105">Applications typically use pop-up windows to briefly display important notification messages to the user.</span></span> <span data-ttu-id="fd371-106">Приложение создает окно, отображает его для определенной в приложении длительности, а затем уничтожает окно.</span><span class="sxs-lookup"><span data-stu-id="fd371-106">An application creates the window, displays it for an application-defined duration, and then destroys the window.</span></span>

<span data-ttu-id="fd371-107">Поскольку пользователям с нарушениями визуального или восприятия может потребоваться больше времени для чтения всплывающих окон уведомлений, приложения не должны жестко закодировать длительность.</span><span class="sxs-lookup"><span data-stu-id="fd371-107">Because users with visual impairments or cognitive conditions might need more time to read notification pop-ups, applications should not hard code the duration.</span></span> <span data-ttu-id="fd371-108">Вместо этого приложение должно установить длительность на основе значения системного параметра **SPI \_ жетмессажедуратион** .</span><span class="sxs-lookup"><span data-stu-id="fd371-108">Instead, an application should set the duration based on the value of the **SPI\_GETMESSAGEDURATION** system parameter.</span></span> <span data-ttu-id="fd371-109">Чтобы получить этот параметр, используйте функцию [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="fd371-109">To retrieve this parameter, use the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="fd371-110">Приложения с поддержкой специальных возможностей могут задавать длительность сообщения на основе вводимых пользователем данных путем установки системного параметра **SPI \_ сетмессажедуратион** .</span><span class="sxs-lookup"><span data-stu-id="fd371-110">Assistive technology applications can set the message duration, based on user input, by setting the **SPI\_SETMESSAGEDURATION** system parameter.</span></span>

 

 