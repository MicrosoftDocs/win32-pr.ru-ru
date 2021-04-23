---
description: Для разработки мониторов используются следующие интерфейсы COM.
ms.assetid: 619991f5-1db1-400a-bf18-d4a6dd6999a8
title: Интерфейсы монитора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66bb06e6153d18c7b0a4291df1c7520380a29844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662446"
---
# <a name="monitor-interfaces"></a><span data-ttu-id="f352c-103">Интерфейсы монитора</span><span class="sxs-lookup"><span data-stu-id="f352c-103">Monitor Interfaces</span></span>

<span data-ttu-id="f352c-104">Для разработки мониторов используются следующие интерфейсы COM.</span><span class="sxs-lookup"><span data-stu-id="f352c-104">The following COM interfaces are used to develop monitors.</span></span>



| <span data-ttu-id="f352c-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f352c-105">Interface</span></span>                              | <span data-ttu-id="f352c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f352c-106">Description</span></span>                                                                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f352c-107">имонитор</span><span class="sxs-lookup"><span data-stu-id="f352c-107">IMonitor</span></span>](imonitor.md)               | <span data-ttu-id="f352c-108">Предоставляет методы, управляющие работой монитора.</span><span class="sxs-lookup"><span data-stu-id="f352c-108">Provides methods that control monitor operation.</span></span> <span data-ttu-id="f352c-109">Этот интерфейс должен быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="f352c-109">This interface must be implemented by the monitor.</span></span>                                                     |
| [<span data-ttu-id="f352c-110">имониторевентер</span><span class="sxs-lookup"><span data-stu-id="f352c-110">IMonitorEventer</span></span>](imonitoreventer.md) | <span data-ttu-id="f352c-111">Предоставляет методы, используемые для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="f352c-111">Provides methods used to send events.</span></span> <span data-ttu-id="f352c-112">Этот интерфейс предоставляется [*службой управления монитором*](m.md) (мксвк).</span><span class="sxs-lookup"><span data-stu-id="f352c-112">This interface is provided by the [*Monitor Control Service*](m.md) (MCSVC).</span></span> |



 

 

 



