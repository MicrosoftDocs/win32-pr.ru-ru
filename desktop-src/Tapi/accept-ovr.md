---
description: В некоторых средах пользователь не предупреждает автоматически о вызове предложения, например, путем звонка или сообщения на экране компьютера.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Принять
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262987"
---
# <a name="accept"></a><span data-ttu-id="29f3d-103">Принять</span><span class="sxs-lookup"><span data-stu-id="29f3d-103">Accept</span></span>

<span data-ttu-id="29f3d-104">В некоторых средах пользователь не предупреждает автоматически о вызове предложения, например, путем звонка или сообщения на экране компьютера.</span><span class="sxs-lookup"><span data-stu-id="29f3d-104">In some environments, a user is not automatically alerted to an offering call, such as by ringing or by a message on their computer screen.</span></span> <span data-ttu-id="29f3d-105">Операция Accept запускает процесс создания предупреждений (как правило, Звонок), и после этого выполняется операция [ответа](answer-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="29f3d-105">The accept operation starts the process of alerting (usually ringing), and the [answer](answer-ovr.md) operation takes place afterward.</span></span> <span data-ttu-id="29f3d-106">Приложение может [Удалить](drop-ovr.md) сеанс, [перенаправить](redirect-ovr.md) его или принять.</span><span class="sxs-lookup"><span data-stu-id="29f3d-106">The application may [drop](drop-ovr.md) the session, [redirect](redirect-ovr.md) it, or accept it.</span></span>

<span data-ttu-id="29f3d-107">Если текущий поставщик услуг поддерживает его, приложение может отправить сведения о пользователе во время принятия.</span><span class="sxs-lookup"><span data-stu-id="29f3d-107">If the current service provider supports it, the application has the option to send user-user information at the time of the accept.</span></span> <span data-ttu-id="29f3d-108">Нет никакой гарантии, что сеть будет предоставлять эту информацию вызывающей стороне.</span><span class="sxs-lookup"><span data-stu-id="29f3d-108">There is no guarantee that the network will deliver this information to the calling party.</span></span>

<span data-ttu-id="29f3d-109">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="29f3d-109">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="29f3d-110">**Интерфейс TAPI 2. x:** См. [**линеакцепт**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span><span class="sxs-lookup"><span data-stu-id="29f3d-110">**TAPI 2.x:** See [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span></span>

 

 
