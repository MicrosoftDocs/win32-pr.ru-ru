---
description: Планшетный ПК включает технологию для взаимодействия с данными пера планшета при их сборе.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Доступ к вводу пера и управление им
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662110"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="20c38-103">Доступ к вводу пера и управление им</span><span class="sxs-lookup"><span data-stu-id="20c38-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="20c38-104">Планшетный ПК включает технологию для взаимодействия с данными пера планшета при их сборе.</span><span class="sxs-lookup"><span data-stu-id="20c38-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="20c38-105">Класс [**RealTimeStylus**](realtimestylus-class.md) является частью стилусинпут прикладных программных интерфейсов (API), которые обеспечивают доступ к потоку данных пера планшета.</span><span class="sxs-lookup"><span data-stu-id="20c38-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="20c38-106">Эти интерфейсы API позволяют записывать, прерывать и изменять поток независимо от подготовки к просмотру и сбору рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="20c38-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="20c38-107">API-интерфейсы Стилусинпут предназначены для:</span><span class="sxs-lookup"><span data-stu-id="20c38-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="20c38-108">Предоставление доступа в режиме реального времени к потоку данных пера планшета.</span><span class="sxs-lookup"><span data-stu-id="20c38-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="20c38-109">Обеспечьте потоку ПОЛЬЗОВАТЕЛЬСКОГО интерфейса блокировку динамической отрисовки рукописных данных, поставляя в очередь данные пакетов в потоке пользовательского интерфейса и делая коллекции рукописного ввода одиночными потоками.</span><span class="sxs-lookup"><span data-stu-id="20c38-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="20c38-110">Повышение производительности и снижение общего использования потоков при использовании объекта [**InkCollector**](inkcollector-class.md) , объекта [**InkOverlay**](inkoverlay-class.md) , элемента управления [InkPicture](inkpicture-control-reference.md) или элемента управления [InkEdit](inkedit-control-reference.md) для накопления рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="20c38-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="20c38-111">API-интерфейсы Стилусинпут не предназначены для работы с объектом [**InkCollector**](inkcollector-class.md) , объектом [**InkOverlay**](inkoverlay-class.md) , элементом управления [InkPicture](inkpicture-control-reference.md) или [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="20c38-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="20c38-112">Если необходимо напрямую взаимодействовать с потоком данных пера планшета или когда приложение может блокировать рукописный ввод в режиме реального времени, используйте объект [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="20c38-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="20c38-113">Используйте объект [**InkCollector**](inkcollector-class.md) , объект [**InkOverlay**](inkoverlay-class.md) , элемент управления [InkPicture](inkpicture-control-reference.md) или элемент управления [InkEdit](inkedit-control-reference.md) , если поведение этих объектов по умолчанию обеспечивает необходимое поведение.</span><span class="sxs-lookup"><span data-stu-id="20c38-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="20c38-114">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="20c38-114">In This Section</span></span>

<span data-ttu-id="20c38-115">В следующих разделах описываются элементы API-интерфейсов Стилусинпут:</span><span class="sxs-lookup"><span data-stu-id="20c38-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="20c38-116">Архитектура API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="20c38-117">Работа с API-интерфейсами Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="20c38-118">Работа с классом RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="20c38-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="20c38-119">Подключаемые модули и класс RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="20c38-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="20c38-120">Данные подключаемого модуля и класс RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="20c38-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="20c38-121">Примечания по реализации для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="20c38-122">Подключаемые модули сбора рукописных данных</span><span class="sxs-lookup"><span data-stu-id="20c38-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="20c38-123">Подключаемые модули динамического рендеринга</span><span class="sxs-lookup"><span data-stu-id="20c38-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="20c38-124">Подключаемые модули распознавателя</span><span class="sxs-lookup"><span data-stu-id="20c38-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="20c38-125">Рекомендации по использованию API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="20c38-126">Рекомендации по проектированию для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="20c38-127">Рекомендации по потокам для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="20c38-128">Модель каскадного RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="20c38-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="20c38-129">Рекомендации по обработке ошибок для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="20c38-130">Рекомендации по повышению производительности для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="20c38-131">Рекомендации по частичному доверию для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="20c38-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="20c38-132">См. также</span><span class="sxs-lookup"><span data-stu-id="20c38-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c38-133">Пример подключаемого модуля RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="20c38-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="20c38-134">Пример коллекции рукописных данных RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="20c38-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



