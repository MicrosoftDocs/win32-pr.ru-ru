---
description: Сведения о функциях, используемых при асинхронном взаимодействии между приложениями и компонентами, размещенными в диспетчере очереди печати.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Функции асинхронной печати уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394859"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="53346-103">Функции асинхронной печати уведомлений</span><span class="sxs-lookup"><span data-stu-id="53346-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="53346-104">Следующие функции используются при асинхронном взаимодействии между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.</span><span class="sxs-lookup"><span data-stu-id="53346-104">The following functions are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53346-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="53346-105">In this section</span></span>



| <span data-ttu-id="53346-106">Функция</span><span class="sxs-lookup"><span data-stu-id="53346-106">Function</span></span>                                                                                        | <span data-ttu-id="53346-107">Описание</span><span class="sxs-lookup"><span data-stu-id="53346-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53346-108">**креатепринтасинкнотифичаннел**</span><span class="sxs-lookup"><span data-stu-id="53346-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="53346-109">Создает коммуникационный канал между компонентом печати, размещенным в очереди печати, например драйвером печати или монитором порта, и приложением, которое получает уведомления от компонента.</span><span class="sxs-lookup"><span data-stu-id="53346-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="53346-110">**регистерфорпринтасинкнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="53346-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="53346-111">Позволяет приложению регистрироваться для получения уведомлений из компонентов печати, размещенных в очереди печати, таких как драйверы принтеров, обработчики печати и мониторы портов.</span><span class="sxs-lookup"><span data-stu-id="53346-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="53346-112">**унрегистерфорпринтасинкнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="53346-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="53346-113">Включает приложение, зарегистрированное для получения уведомлений от компонентов печати, размещаемых диспетчером очереди печати, для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="53346-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




