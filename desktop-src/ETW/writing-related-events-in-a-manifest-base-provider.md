---
description: Используйте функцию EventWriteTransfer, когда нескольким компонентам нужно связать свои события в сквозном сценарии трассировки.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Запись связанных событий в поставщик на основе манифеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543066"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="41afe-103">Запись связанных событий в поставщик на основе манифеста</span><span class="sxs-lookup"><span data-stu-id="41afe-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="41afe-104">Используйте функцию [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) , когда нескольким компонентам нужно связать свои события в сквозном сценарии трассировки.</span><span class="sxs-lookup"><span data-stu-id="41afe-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="41afe-105">Например, компоненты A, B и C выполняют работу над связанным действием и хотят связать все события, связанные с этим действием.</span><span class="sxs-lookup"><span data-stu-id="41afe-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="41afe-106">ETW использует локальное хранилище потока, чтобы сделать идентификатор действия предыдущего компонента доступным следующему компоненту.</span><span class="sxs-lookup"><span data-stu-id="41afe-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="41afe-107">Компонент извлекает идентификатор предыдущего компонента из локального хранилища и присваивает ему идентификатор связанного действия.</span><span class="sxs-lookup"><span data-stu-id="41afe-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="41afe-108">Затем потребитель может использовать связанный идентификатор действия для прохода по цепочке событий от одного компонента к другому.</span><span class="sxs-lookup"><span data-stu-id="41afe-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



