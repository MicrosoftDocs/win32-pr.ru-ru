---
description: Обзор уведомления о событиях
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Обзор уведомления о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806076"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="fdab2-103">Обзор уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="fdab2-103">Overview of Event Notification</span></span>

<span data-ttu-id="fdab2-104">Фильтр Уведомляет диспетчер графа фильтра о событии, публикуя уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="fdab2-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="fdab2-105">Событие может быть ожидаемым, например концом потока, или сообщением об ошибке, например при сбое визуализации потока.</span><span class="sxs-lookup"><span data-stu-id="fdab2-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="fdab2-106">Диспетчер графов фильтров обрабатывает некоторые события фильтра по отдельности и оставляет другим приложениям возможность обработки.</span><span class="sxs-lookup"><span data-stu-id="fdab2-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="fdab2-107">Если диспетчер графов фильтров не обрабатывает событие фильтра, уведомление о событии помещается в очередь.</span><span class="sxs-lookup"><span data-stu-id="fdab2-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="fdab2-108">Граф фильтра также может ставить в очередь собственные уведомления о событиях для приложения.</span><span class="sxs-lookup"><span data-stu-id="fdab2-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="fdab2-109">Приложение получает события из очереди и реагирует на них в зависимости от типа события.</span><span class="sxs-lookup"><span data-stu-id="fdab2-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="fdab2-110">Уведомление о событии в DirectShow, таким образом, аналогично схеме очереди сообщений Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fdab2-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="fdab2-111">Приложение также может отменить поведение диспетчера графа фильтра по умолчанию для данного типа событий.</span><span class="sxs-lookup"><span data-stu-id="fdab2-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="fdab2-112">Затем Диспетчер графа фильтров помещает эти события непосредственно в очередь, чтобы приложение было обработано.</span><span class="sxs-lookup"><span data-stu-id="fdab2-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="fdab2-113">Этот механизм позволяет</span><span class="sxs-lookup"><span data-stu-id="fdab2-113">This mechanism enables</span></span>

-   <span data-ttu-id="fdab2-114">Диспетчер графа фильтров для взаимодействия с приложением.</span><span class="sxs-lookup"><span data-stu-id="fdab2-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="fdab2-115">Фильтры для взаимодействия с приложением и диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="fdab2-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="fdab2-116">Приложение для определения степени участия в обработке событий.</span><span class="sxs-lookup"><span data-stu-id="fdab2-116">The application to determine its degree of involvement in handling events.</span></span>

 

 



