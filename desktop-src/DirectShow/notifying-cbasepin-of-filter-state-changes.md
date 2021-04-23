---
description: Уведомление Кбасепин об изменениях состояния фильтра
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Уведомление Кбасепин об изменениях состояния фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341752"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="df326-103">Уведомление Кбасепин об изменениях состояния фильтра</span><span class="sxs-lookup"><span data-stu-id="df326-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="df326-104">Класс **кбасепин** уведомляется всякий раз, когда изменяется состояние фильтра владельца.</span><span class="sxs-lookup"><span data-stu-id="df326-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="df326-105">Для каждого перехода состояния фильтр вызывает соответствующий метод для ПИН-кода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="df326-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="df326-106">Новое состояние фильтра</span><span class="sxs-lookup"><span data-stu-id="df326-106">New Filter State</span></span> | <span data-ttu-id="df326-107">Метод Кбасепин</span><span class="sxs-lookup"><span data-stu-id="df326-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="df326-108">Остановлена</span><span class="sxs-lookup"><span data-stu-id="df326-108">Stopped</span></span>          | [<span data-ttu-id="df326-109">**Кбасепин:: Inactive**</span><span class="sxs-lookup"><span data-stu-id="df326-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="df326-110">Пауза</span><span class="sxs-lookup"><span data-stu-id="df326-110">Paused</span></span>           | [<span data-ttu-id="df326-111">**Кбасепин:: Active**</span><span class="sxs-lookup"><span data-stu-id="df326-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="df326-112">Запущен</span><span class="sxs-lookup"><span data-stu-id="df326-112">Running</span></span>          | [<span data-ttu-id="df326-113">**Кбасепин:: Run**</span><span class="sxs-lookup"><span data-stu-id="df326-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="df326-114">Производный класс должен переопределять эти методы для реагирования на изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="df326-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="df326-115">В зависимости от фильтра ПИН-код может запустить рабочий поток, который доставляет примеры, зафиксировать или отменять выделение памяти и т. д.</span><span class="sxs-lookup"><span data-stu-id="df326-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



