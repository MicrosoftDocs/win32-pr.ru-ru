---
description: Ниже приведены рекомендации по работе с потоками для планшетных ПК, связанные с использованием модели COM и автоматизации.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Рекомендации по потокам COM и автоматизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701351"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="0bc10-103">Рекомендации по потокам COM и автоматизации</span><span class="sxs-lookup"><span data-stu-id="0bc10-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="0bc10-104">Ниже приведены рекомендации по работе с потоками для планшетных ПК, связанные с использованием модели COM и автоматизации.</span><span class="sxs-lookup"><span data-stu-id="0bc10-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="0bc10-105">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="0bc10-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="0bc10-106">Приложения STA и MTA</span><span class="sxs-lookup"><span data-stu-id="0bc10-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="0bc10-107">InkCollector и InkOverlay</span><span class="sxs-lookup"><span data-stu-id="0bc10-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="0bc10-108">Приемники событий</span><span class="sxs-lookup"><span data-stu-id="0bc10-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="0bc10-109">Исключения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="0bc10-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="0bc10-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc10-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="0bc10-111">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="0bc10-111">Thread Safety</span></span>

<span data-ttu-id="0bc10-112">Объекты планшетных ПК, за исключением элементов управления [InkPicture](inkpicture-control.md) и [InkEdit](inkedit-control.md) , являются потокобезопасными и помечаются как оба.</span><span class="sxs-lookup"><span data-stu-id="0bc10-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="0bc10-113">Как и то, и другое, они могут работать в одном потоковом апартаменте (STA) или в многопоточном апартаменте (MTA).</span><span class="sxs-lookup"><span data-stu-id="0bc10-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="0bc10-114">В Windows Forms используется модель STA, поскольку Windows Forms основана на собственных окнах Win32, которые по сути являются потоковыми потоками.</span><span class="sxs-lookup"><span data-stu-id="0bc10-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="0bc10-115">Приложения STA и MTA</span><span class="sxs-lookup"><span data-stu-id="0bc10-115">STA and MTA Applications</span></span>

<span data-ttu-id="0bc10-116">Если приложение выполняется в MTA или использует бесплатный потоковый маршалеру (FTM), необходимо написать потокобезопасный код. Тем не менее, это позволяет повысить производительность обработки определенных событий.</span><span class="sxs-lookup"><span data-stu-id="0bc10-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="0bc10-117">InkCollector и InkOverlay</span><span class="sxs-lookup"><span data-stu-id="0bc10-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="0bc10-118">Приложение не должно освобождать его окончательную ссылку на объект [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) , тем самым уничтожая объект непосредственно из потока рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="0bc10-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="0bc10-119">Вместо этого приложение должно освободить объект **InkCollector** или **InkOverlay** из потока приложения.</span><span class="sxs-lookup"><span data-stu-id="0bc10-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="0bc10-120">**Внимание!** Приложение, помеченное как MTA или использующее FTM, которое позволяет выполнять прямые вызовы из потока рукописного ввода в подразделение приложения, может освобождать последнюю ссылку на объект [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) непосредственно из потока рукописного ввода; Однако это приводит к неустранимому сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="0bc10-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="0bc10-121">Приемники событий</span><span class="sxs-lookup"><span data-stu-id="0bc10-121">Event Sinks</span></span>

<span data-ttu-id="0bc10-122">Если приложение не использует FTM, а объект и его приемник событий создаются в разных апартаментах, то событие выполняется в потоке, обслуживающем приемник событий.</span><span class="sxs-lookup"><span data-stu-id="0bc10-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="0bc10-123">Исключения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="0bc10-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="0bc10-124">Исключения, вызванные из обработчиков событий планшетных ПК, используются и не видны остальным или вашим приложениям.</span><span class="sxs-lookup"><span data-stu-id="0bc10-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="0bc10-125">Аналогичным образом значения HRESULT не распространяются на обработчики событий планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="0bc10-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="0bc10-126">Если приложение, использующее уровень COM, создает исключение, фоновый поток завершается, и исключение будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="0bc10-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="0bc10-127">Никакие дополнительные обработчики событий не будут вызываться.</span><span class="sxs-lookup"><span data-stu-id="0bc10-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bc10-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc10-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc10-129">Пример приемников событий C++</span><span class="sxs-lookup"><span data-stu-id="0bc10-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="0bc10-130">Общие рекомендации по потокам</span><span class="sxs-lookup"><span data-stu-id="0bc10-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="0bc10-131">Рекомендации по потокам управляемых библиотек</span><span class="sxs-lookup"><span data-stu-id="0bc10-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 



