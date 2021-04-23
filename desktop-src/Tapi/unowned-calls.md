---
description: Чтобы предотвратить ненадлежащие вызовы в системе телефонии, TAPI удаляет вызовы, которые получили сигнал от поставщика услуг, если не удается опознать приложение для первоначального владельца вызова.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Ненадлежащие вызовы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673325"
---
# <a name="unowned-calls"></a><span data-ttu-id="9a0c1-103">Ненадлежащие вызовы</span><span class="sxs-lookup"><span data-stu-id="9a0c1-103">Unowned Calls</span></span>

<span data-ttu-id="9a0c1-104">Чтобы предотвратить ненадлежащие вызовы в системе телефонии, TAPI удаляет вызовы, которые получили сигнал от поставщика услуг, если не удается опознать приложение для первоначального владельца вызова.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-104">To prevent unowned calls from being in the telephony system, TAPI drops calls that have been signaled up from a service provider if it cannot identify an application to be the initial owner of the call.</span></span> <span data-ttu-id="9a0c1-105">В TAPI версии 2,0 и более поздних интерфейс TAPI вызывает функцию [**тспи \_ линедроп**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) для удаления вызова.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-105">In TAPI version 2.0 and later, TAPI calls the [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) function to drop the call.</span></span>

<span data-ttu-id="9a0c1-106">Поставщик услуг может заранее определить, доступно ли приложение, чтобы стать владельцем нового вызова.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-106">The service provider can know in advance whether or not there is an application available to take ownership of a new call.</span></span> <span data-ttu-id="9a0c1-107">TAPI всегда информирует поставщика служб о типах носителей, для которых доступно приложение с помощью функции [**\_ линесетдефаултмедиадетектион тспи**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .</span><span class="sxs-lookup"><span data-stu-id="9a0c1-107">TAPI always informs the service provider of the media types for which there is an application available by using the [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) function.</span></span>

<span data-ttu-id="9a0c1-108">Например, если поставщик услуг определяет, что имеется активный вызов в строке, имеющей \_ режим линемедиамоде интерактивевоице, он должен проверить обнаружение носителей по умолчанию перед созданием [**строк \_ невкалл**](line-newcall.md) и [**Line \_ каллстате**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-108">For example, if a service provider determines that there is an active call on the line having LINEMEDIAMODE\_INTERACTIVEVOICE mode, it should check the default media detection before generating the [**LINE\_NEWCALL**](line-newcall.md) and [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span></span> <span data-ttu-id="9a0c1-109">Если обнаружение носителей по умолчанию показывает, что ни одно приложение не ищет \_ вызов ИНТЕРАКТИВЕВОИЦЕ линемедиамоде, поставщик услуг не должен отправить сообщения, так как TAPI немедленно отправит его.</span><span class="sxs-lookup"><span data-stu-id="9a0c1-109">If the default media detection shows that no application is looking for a LINEMEDIAMODE\_INTERACTIVEVOICE call, the service provider should not send the messages because TAPI will immediately drop it.</span></span>

 

 
