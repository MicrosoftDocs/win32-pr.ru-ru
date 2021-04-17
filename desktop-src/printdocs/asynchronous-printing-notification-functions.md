---
description: Следующие интерфейсы используются для асинхронного взаимодействия между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Функции асинхронной печати уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693575"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="ee9f9-103">Функции асинхронной печати уведомлений</span><span class="sxs-lookup"><span data-stu-id="ee9f9-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="ee9f9-104">Следующие интерфейсы используются для асинхронного взаимодействия между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.</span><span class="sxs-lookup"><span data-stu-id="ee9f9-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ee9f9-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ee9f9-105">In this section</span></span>



| <span data-ttu-id="ee9f9-106">Функция</span><span class="sxs-lookup"><span data-stu-id="ee9f9-106">Function</span></span>                                                                                        | <span data-ttu-id="ee9f9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ee9f9-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee9f9-108">**креатепринтасинкнотифичаннел**</span><span class="sxs-lookup"><span data-stu-id="ee9f9-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="ee9f9-109">Создает коммуникационный канал между компонентом печати, размещенным в очереди печати, например драйвером печати или монитором порта, и приложением, которое получает уведомления от компонента.</span><span class="sxs-lookup"><span data-stu-id="ee9f9-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="ee9f9-110">**регистерфорпринтасинкнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="ee9f9-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="ee9f9-111">Позволяет приложению регистрироваться для получения уведомлений из компонентов печати, размещенных в очереди печати, таких как драйверы принтеров, обработчики печати и мониторы портов.</span><span class="sxs-lookup"><span data-stu-id="ee9f9-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="ee9f9-112">**унрегистерфорпринтасинкнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="ee9f9-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="ee9f9-113">Включает приложение, зарегистрированное для получения уведомлений от компонентов печати, размещаемых диспетчером очереди печати, для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="ee9f9-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




