---
description: Следующие перечисления используются при асинхронном взаимодействии между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Асинхронные перечисления уведомлений о печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702204"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="51c27-103">Асинхронные перечисления уведомлений о печати</span><span class="sxs-lookup"><span data-stu-id="51c27-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="51c27-104">Следующие перечисления используются при асинхронном взаимодействии между приложениями и компонентами, размещенными в диспетчере очереди печати, например драйверами принтеров и мониторами портов.</span><span class="sxs-lookup"><span data-stu-id="51c27-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51c27-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="51c27-105">In this section</span></span>



| <span data-ttu-id="51c27-106">Перечисление</span><span class="sxs-lookup"><span data-stu-id="51c27-106">Enumeration</span></span>                                                                               | <span data-ttu-id="51c27-107">Описание</span><span class="sxs-lookup"><span data-stu-id="51c27-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51c27-108">**принтасинкнотификонверсатионстиле**</span><span class="sxs-lookup"><span data-stu-id="51c27-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="51c27-109">Указывает, является ли связь двунаправленной или однонаправленной между приложениями и диспетчером очереди печати, такими компонентами, как драйверы принтеров, обработчики печати и мониторы портов.</span><span class="sxs-lookup"><span data-stu-id="51c27-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="51c27-110">**принтасинкнотиферрор**</span><span class="sxs-lookup"><span data-stu-id="51c27-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="51c27-111">Указывает часть кода ошибки **HRESULT** , возвращаемую после асинхронного сбоя уведомления.</span><span class="sxs-lookup"><span data-stu-id="51c27-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="51c27-112">**принтасинкнотифюсерфилтер**</span><span class="sxs-lookup"><span data-stu-id="51c27-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="51c27-113">Указывает, будут ли уведомления переключаться только на прослушивание приложений, связанных с тем же пользователем, что и отправитель, размещенный в очереди печати, или к более широкому набору прослушивающих приложений.</span><span class="sxs-lookup"><span data-stu-id="51c27-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




