---
description: Предоставляет доступ к событиям пера, поступающим от пера или сенсорных дигитайзеров.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Ссылка RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265452"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="76721-103">Ссылка RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="76721-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="76721-104">Предоставляет доступ к событиям пера, поступающим от пера или сенсорных дигитайзеров.</span><span class="sxs-lookup"><span data-stu-id="76721-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76721-105">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="76721-105">In This Section</span></span>

-   [<span data-ttu-id="76721-106">Классы и интерфейсы RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="76721-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="76721-107">Перечисления RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="76721-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="76721-108">Структуры RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="76721-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="76721-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76721-109">Remarks</span></span>

<span data-ttu-id="76721-110">Этот объект реализует COM-интерфейс [**иреалтиместилус**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="76721-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="76721-111">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.</span><span class="sxs-lookup"><span data-stu-id="76721-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="76721-112">Можно полностью управлять, динамически подготавливать, изменять и даже удалять данные из потока пакетов в синхронных и асинхронных подключаемых модулях объекта [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="76721-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="76721-113">Перо в реальном времени предоставляет способ создания объекта **инкколлектинг** , который является однопотоковым и резидентным в ПОТОКЕ пользовательского интерфейса приложения.</span><span class="sxs-lookup"><span data-stu-id="76721-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="76721-114">Этот объект **инкколлектинг** получает доступ к данным пера в реальном времени из очереди.</span><span class="sxs-lookup"><span data-stu-id="76721-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="76721-115">Объект **инкколлектинг** в сочетании с пером в режиме реального времени позволяет изменять выбор в режиме реального времени и изменять собранные данные рукописного ввода в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="76721-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="76721-116">Дополнительные сведения см. в разделе [доступ к вводу пера и управление](accessing-and-manipulating-stylus-input.md)им.</span><span class="sxs-lookup"><span data-stu-id="76721-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="76721-117">Используйте объект [**класса RealTimeStylus**](realtimestylus-class.md) , чтобы напрямую взаимодействовать с потоком данных пера планшета или блокировать рукописный ввод в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="76721-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="76721-118">Используйте объект [**класса InkCollector**](inkcollector-class.md) , объект [**класса InkOverlay**](inkoverlay-class.md) , элемент управления [InkPicture](inkpicture-control-reference.md) или элемент управления [InkEdit](inkedit-control-reference.md) , если поведение этих объектов по умолчанию обеспечивает необходимое поведение.</span><span class="sxs-lookup"><span data-stu-id="76721-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="76721-119">События пера в реальном времени находятся в определенном обработчике окна в пределах определенного прямоугольника ввода окна.</span><span class="sxs-lookup"><span data-stu-id="76721-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="76721-120">Реалтиместилуссервице может передавать данные пера в несколько объектов [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="76721-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="76721-121">Каждый объект **класса RealTimeStylus** получает данные пера для определенного раздела окна на основе определенного [**Свойства Иреалтиместилус:: виндовинпутректангле**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) для этого объекта **класса RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="76721-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="76721-122">Объект **класса RealTimeStylus** получает данные пера, а затем обрабатывает его через список синхронных и асинхронных подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="76721-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="76721-123">Разница между синхронными подключаемыми модулями и асинхронными подключаемыми модулями заключается в потоке, в котором они выполняются, и в вызывающей последовательности.</span><span class="sxs-lookup"><span data-stu-id="76721-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="76721-124">Синхронные подключаемые модули вызываются потоком, в котором выполняется объект [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="76721-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="76721-125">Каждый раз при создании экземпляра объекта **класса RealTimeStylus** создается экземпляр потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="76721-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="76721-126">Синхронные подключаемые модули выполняются в этом новом потоке, созданном для экземпляра объекта **класса RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="76721-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="76721-127">Асинхронные подключаемые модули вызываются через пользовательский интерфейс или поток приложения после обработки потока пакетов синхронными подключаемыми модулями и хранятся в очереди вывода.</span><span class="sxs-lookup"><span data-stu-id="76721-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76721-128">См. также</span><span class="sxs-lookup"><span data-stu-id="76721-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76721-129">**Интерфейс Идинамикрендерер**</span><span class="sxs-lookup"><span data-stu-id="76721-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="76721-130">**истилуссинкплугин**</span><span class="sxs-lookup"><span data-stu-id="76721-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="76721-131">**истилусасинкплугин**</span><span class="sxs-lookup"><span data-stu-id="76721-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="76721-132">**иреалтиместилус**</span><span class="sxs-lookup"><span data-stu-id="76721-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
