---
description: Класс Каммсжевент является оболочкой для объектов событий, выполняющих обработку сообщений.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Класс Каммсжевент (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668721"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="bdfc9-103">Класс Каммсжевент</span><span class="sxs-lookup"><span data-stu-id="bdfc9-103">CAMMsgEvent class</span></span>

![Иерархия классов каммсжевент](images/util06.png)

<span data-ttu-id="bdfc9-105">`CAMMsgEvent`Класс является оболочкой для объектов событий, выполняющих обработку сообщений.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="bdfc9-106">Этот класс является производным от объекта [**камевент**](camevent.md) .</span><span class="sxs-lookup"><span data-stu-id="bdfc9-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="bdfc9-107">Он добавляет один метод [**каммсжевент:: ваитмсг**](cammsgevent-waitmsg.md), который отправляет входящие сообщения в ожидании.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="bdfc9-108">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="bdfc9-108">Public Methods</span></span>                                 | <span data-ttu-id="bdfc9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bdfc9-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="bdfc9-110">**каммсжевент**</span><span class="sxs-lookup"><span data-stu-id="bdfc9-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="bdfc9-111">Конструктор.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="bdfc9-112">**ваитмсг**</span><span class="sxs-lookup"><span data-stu-id="bdfc9-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="bdfc9-113">Ожидает получения сигнала о событии, а также при диспетчеризации отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="bdfc9-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bdfc9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bdfc9-114">Requirements</span></span>



| <span data-ttu-id="bdfc9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bdfc9-115">Requirement</span></span> | <span data-ttu-id="bdfc9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bdfc9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfc9-117">Header</span><span class="sxs-lookup"><span data-stu-id="bdfc9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bdfc9-118"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdfc9-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bdfc9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bdfc9-119">Library</span></span><br/> | <dl> <span data-ttu-id="bdfc9-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bdfc9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




