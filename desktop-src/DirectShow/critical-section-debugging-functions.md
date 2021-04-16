---
description: Функции отладки критического раздела
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Функции отладки критического раздела
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536896"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="235e7-103">Функции отладки критического раздела</span><span class="sxs-lookup"><span data-stu-id="235e7-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="235e7-104">Эти функции помогают отлаживать критически важные разделы в коде, что может упростить поиск причины взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="235e7-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="235e7-105">Эти функции используют вспомогательный класс [**ккритсек**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="235e7-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="235e7-106">Функция</span><span class="sxs-lookup"><span data-stu-id="235e7-106">Function</span></span>                             | <span data-ttu-id="235e7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="235e7-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="235e7-108">**критчеккин**</span><span class="sxs-lookup"><span data-stu-id="235e7-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="235e7-109">Возвращает **значение true** , если текущий поток владеет заданной критической секцией.</span><span class="sxs-lookup"><span data-stu-id="235e7-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="235e7-110">**критчеккаут**</span><span class="sxs-lookup"><span data-stu-id="235e7-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="235e7-111">Возвращает **значение false** , если текущий поток владеет заданной критической секцией.</span><span class="sxs-lookup"><span data-stu-id="235e7-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="235e7-112">**дбглокктраце**</span><span class="sxs-lookup"><span data-stu-id="235e7-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="235e7-113">Включает или отключает ведение журнала отладки для заданной критической секции.</span><span class="sxs-lookup"><span data-stu-id="235e7-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="235e7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="235e7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="235e7-115">Отладка служебных программ</span><span class="sxs-lookup"><span data-stu-id="235e7-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



