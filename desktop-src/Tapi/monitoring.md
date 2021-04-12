---
description: Наблюдение — это определяемая поставщиком услуг функция, которая обнаруживает сигналы, указывающие на другие носители.
ms.assetid: 77735a42-049a-4f16-a502-ff6d31ef3cd0
title: Наблюдение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1bca5e4287d0aeb3aee89cceb72f725e95a3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344262"
---
# <a name="monitoring"></a><span data-ttu-id="cd4fc-103">Наблюдение</span><span class="sxs-lookup"><span data-stu-id="cd4fc-103">Monitoring</span></span>

<span data-ttu-id="cd4fc-104">Наблюдение — это определяемая поставщиком услуг функция, которая обнаруживает сигналы, указывающие на другие носители.</span><span class="sxs-lookup"><span data-stu-id="cd4fc-104">Monitoring is a service-provider defined feature that detects signals that indicate other media.</span></span> <span data-ttu-id="cd4fc-105">Например, одно приложение может воспроизводить исходящее голосовое сообщение "оставлять сообщение", пока входящий вызов начинает отправку факса "Звонок" и ожидает подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cd4fc-105">For example, one application can be playing an outgoing "leave a message" voice message while the incoming call starts sending a fax "calling" tone and waits for a handshake.</span></span> <span data-ttu-id="cd4fc-106">Чтобы не потерять вызов факса, локальное приложение отслеживает этот тон при воспроизведении речевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="cd4fc-106">In order not to lose the fax call, the local application monitors for this tone while playing the voice message.</span></span>

<span data-ttu-id="cd4fc-107">Мониторинг включает в себя [мониторинг носителей](/previous-versions/windows/desktop/legacy/ms725242(v=vs.85)), [Отслеживание цифр](/previous-versions/windows/desktop/legacy/ms725185(v=vs.85))и [мониторинг тона](/previous-versions/windows/desktop/legacy/ms725520(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd4fc-107">Monitoring comprises [media monitoring](/previous-versions/windows/desktop/legacy/ms725242(v=vs.85)), [digit monitoring](/previous-versions/windows/desktop/legacy/ms725185(v=vs.85)), and [tone monitoring](/previous-versions/windows/desktop/legacy/ms725520(v=vs.85)).</span></span>

 

 
