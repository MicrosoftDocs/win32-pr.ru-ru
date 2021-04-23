---
description: В исходном интерфейсе сокета программного распространения Berkeley (BSD) функция Select была стандартной (и только) означает получение сетевых событий.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Бирает
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702011"
---
# <a name="selects"></a><span data-ttu-id="16b54-103">Бирает</span><span class="sxs-lookup"><span data-stu-id="16b54-103">Selects</span></span>

<span data-ttu-id="16b54-104">В исходном интерфейсе сокета программного распространения Berkeley (BSD) функция [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) была стандартной (и только) означает получение сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="16b54-104">In the original Berkeley Software Distribution (BSD) socket interface the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was the standard (and only) means to obtain network event indications.</span></span> <span data-ttu-id="16b54-105">Для каждого сокета можно выполнить опрос или ожидание сведений о состоянии чтения, записи или ошибки.</span><span class="sxs-lookup"><span data-stu-id="16b54-105">For each socket, information on read, write, or error status can be polled or waited on.</span></span> <span data-ttu-id="16b54-106">Дополнительные сведения см. в разделе [**вспселект**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="16b54-106">See [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) for more information.</span></span> <span data-ttu-id="16b54-107">Обратите внимание, что \_ этот подход не позволяет получить качество обслуживания с помощью фильтра событий сети.</span><span class="sxs-lookup"><span data-stu-id="16b54-107">Note that network event FD\_QOS cannot be obtained by this approach.</span></span>

 

 
