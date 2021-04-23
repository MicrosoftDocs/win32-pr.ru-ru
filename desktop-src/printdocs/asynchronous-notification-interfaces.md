---
description: Следующие интерфейсы используются для асинхронного взаимодействия между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Интерфейсы асинхронного уведомления о печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817768"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="79bcd-103">Интерфейсы асинхронного уведомления о печати</span><span class="sxs-lookup"><span data-stu-id="79bcd-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="79bcd-104">Следующие интерфейсы используются для асинхронного взаимодействия между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.</span><span class="sxs-lookup"><span data-stu-id="79bcd-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="79bcd-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="79bcd-105">In this section</span></span>



| <span data-ttu-id="79bcd-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="79bcd-106">Interface</span></span>                                                                     | <span data-ttu-id="79bcd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="79bcd-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79bcd-108">**ипринтасинкнотификаллбакк**</span><span class="sxs-lookup"><span data-stu-id="79bcd-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="79bcd-109">Создает канал связи, используемый приложениями и компонентами, размещенными в диспетчере очереди печати, и управляет им.</span><span class="sxs-lookup"><span data-stu-id="79bcd-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="79bcd-110">**ипринтасинкнотифичаннел**</span><span class="sxs-lookup"><span data-stu-id="79bcd-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="79bcd-111">Представляет канал связи, который компоненты, размещенные диспетчером очереди печати, используют для отправки уведомлений в приложения.</span><span class="sxs-lookup"><span data-stu-id="79bcd-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="79bcd-112">Если канал является двунаправленным, приложения могут использовать тот же канал для отправки ответов обратно в компонент.</span><span class="sxs-lookup"><span data-stu-id="79bcd-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="79bcd-113">**ипринтасинкнотифидатаобжект**</span><span class="sxs-lookup"><span data-stu-id="79bcd-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="79bcd-114">Инкапсулирует данные, отправленные в канале уведомлений.</span><span class="sxs-lookup"><span data-stu-id="79bcd-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




