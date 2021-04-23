---
description: Объект RealTimeStylus предназначен для предоставления доступа к потоку данных из пера планшета в режиме реального времени.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Подключаемые модули и класс RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693660"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="869ab-103">Подключаемые модули и класс RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="869ab-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="869ab-104">Объект [**RealTimeStylus**](realtimestylus-class.md) предназначен для предоставления доступа к потоку данных из пера планшета в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="869ab-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="869ab-105">Подключаемые модули, реализующие интерфейс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) или [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , можно добавить в объект **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="869ab-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="869ab-106">Синхронные подключаемые модули, как правило, вызываются непосредственно объектом **RealTimeStylus** в потоке с высоким приоритетом, а Асинхронные подключаемые модули обычно вызываются в потоке пользовательского интерфейса приложения.</span><span class="sxs-lookup"><span data-stu-id="869ab-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="869ab-107">Создайте или используйте синхронные подключаемые модули для задач, которым требуется доступ к потоку данных в режиме реального времени и которые не требуют вычисления, например фильтрация пакетов.</span><span class="sxs-lookup"><span data-stu-id="869ab-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="869ab-108">Создайте или используйте асинхронные подключаемые модули для задач, не требующих доступа в режиме реального времени к потоку данных, например коллекции рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="869ab-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="869ab-109">Некоторые задачи могут быть требовательными к вычислительным операциям, но они требуют доступа к потоку данных в режиме реального времени, например для распознавания жестов с несколькими штрихами.</span><span class="sxs-lookup"><span data-stu-id="869ab-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="869ab-110">Для решения этих задач интерфейсы API Стилусинпут обеспечивают каскадную модель [**RealTimeStylus**](realtimestylus-class.md) , которая позволяет использовать два объекта **RealTimeStylus** , каждый из которых выполняется в собственном потоке.</span><span class="sxs-lookup"><span data-stu-id="869ab-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="869ab-111">Дополнительные сведения о каскадной модели **RealTimeStylus** см. в статье [каскадная модель RealTimeStylus](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="869ab-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="869ab-112">Интерфейсы [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) и [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) определяют одни и те же методы.</span><span class="sxs-lookup"><span data-stu-id="869ab-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="869ab-113">Эти методы позволяют объекту [**RealTimeStylus**](realtimestylus-class.md) передавать данные пера каждому подключаемому модулю независимо от того, является ли это асинхронным или синхронным подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="869ab-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="869ab-114">Свойства [Microsoft. стилусинпут. истилуссинкплугин.](/previous-versions/ms824752(v=msdn.10)) и [Microsoft. стилусинпут. истилусасинкплугин.](/previous-versions/ms824769(v=msdn.10)) позволяют каждому подключаемому модулю подписываться на определенные данные в потоке данных пера планшета.</span><span class="sxs-lookup"><span data-stu-id="869ab-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="869ab-115">Подключаемый модуль должен подписываться только на данные, необходимые для выполнения задачи, минимизируя требования к производительности.</span><span class="sxs-lookup"><span data-stu-id="869ab-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="869ab-116">Дополнительные сведения о потоках и классе **RealTimeStylus** см. в разделе [вопросы использования потоков для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="869ab-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="869ab-117">Объект [**RealTimeStylus**](realtimestylus-class.md) использует объекты из пространства имен [Microsoft. стилусинпут. плугиндата](/previous-versions/ms823992(v=msdn.10)) для передачи данных пера в подключаемые модули. Объект **RealTimeStylus** также перехватывает исключения, вызываемые подключаемыми модулями. Когда объект **RealTimeStylus** перехватывает исключения, он уведомляет подключаемые модули, вызывая метод [истилуссинкплугин. Error](/previous-versions/ms824754(v=msdn.10)) или [истилусасинкплугин. Error](/previous-versions/ms824771(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="869ab-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="869ab-118">Дополнительные сведения об использовании подключаемых модулей данных см. в разделе [подключаемые модули данных и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="869ab-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="869ab-119">Дополнительные сведения об обработке ошибок см. в разделе [рекомендации по обработке ошибок для API-интерфейсов стилусинпут](error-handling-considerations-for-the-stylusinput-apis.md) и секции данных об ошибках подключаемых модулей данных и класса RealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="869ab-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="869ab-120">По крайней мере один подключаемый модуль должен быть присоединен к объекту [**RealTimeStylus**](realtimestylus-class.md) , прежде чем можно будет включить объект **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="869ab-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="869ab-121">В следующих разделах описаны некоторые распространенные категории подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="869ab-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="869ab-122">Подключаемые модули сбора рукописных данных</span><span class="sxs-lookup"><span data-stu-id="869ab-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="869ab-123">Подключаемые модули динамического рендеринга</span><span class="sxs-lookup"><span data-stu-id="869ab-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="869ab-124">Подключаемые модули распознавателя</span><span class="sxs-lookup"><span data-stu-id="869ab-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="869ab-125">Особые рекомендации</span><span class="sxs-lookup"><span data-stu-id="869ab-125">Special Considerations</span></span>

<span data-ttu-id="869ab-126">Из-за сложной природы объекта [**RealTimeStylus**](realtimestylus-class.md) следует обратить внимание на следующее.</span><span class="sxs-lookup"><span data-stu-id="869ab-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="869ab-127">Объект [**RealTimeStylus**](realtimestylus-class.md) создает исключение, если подключаемый модуль изменяет коллекцию подключаемых модулей, к которой он присоединен.</span><span class="sxs-lookup"><span data-stu-id="869ab-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="869ab-128">Это происходит только в том случае, если подключаемый модуль делает это, пока он вызывается объектом **RealTimeStylus** как членом этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="869ab-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="869ab-129">Следующий пример на языке C \# — это код, который заставляет объект [**RealTimeStylus**](realtimestylus-class.md) вызывать исключение.</span><span class="sxs-lookup"><span data-stu-id="869ab-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



<span data-ttu-id="869ab-130">Объект [**RealTimeStylus**](realtimestylus-class.md) создает исключение, если подключаемый модуль вызывает метод [Dispose](/previous-versions/ms825891(v=msdn.10)) объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="869ab-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="869ab-131">Это происходит только в том случае, если подключаемый модуль делает это, пока он вызывается объектом **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="869ab-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="869ab-132">Следующий пример на языке C \# — это код, который заставляет объект [**RealTimeStylus**](realtimestylus-class.md) вызывать исключение.</span><span class="sxs-lookup"><span data-stu-id="869ab-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



<span data-ttu-id="869ab-133">Коллекции подключаемых модулей можно изменить, пока включен объект [**RealTimeStylus**](realtimestylus-class.md) . Однако это может усложнить работу приложения в прогнозировании.</span><span class="sxs-lookup"><span data-stu-id="869ab-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="869ab-134">Когда подключаемый модуль добавляется, когда объект **RealTimeStylus** включен, объект **RealTimeStylus** вызывает метод [истилусасинкплугин. реалтиместилусенаблед](/previous-versions/ms824775(v=msdn.10)) или [истилуссинкплугин. реалтиместилусенаблед](/previous-versions/ms824758(v=msdn.10)) подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="869ab-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="869ab-135">Когда подключаемый модуль удаляется, пока включен объект **RealTimeStylus** , объект **RealTimeStylus** вызывает метод [истилусасинкплугин. реалтиместилусдисаблед](/previous-versions/ms824774(v=msdn.10)) или [истилуссинкплугин. реалтиместилусдисаблед](/previous-versions/ms824757(v=msdn.10)) подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="869ab-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="869ab-136">Это позволяет подключаемому модулю поддерживать свое правильное состояние без проверки свойства [Enabled](/previous-versions/ms824832(v=msdn.10)) объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="869ab-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="869ab-137">При добавлении подключаемого модуля, когда включен объект [**RealTimeStylus**](realtimestylus-class.md) , подключаемые данные, которые получает подключаемый модуль, могут не содержать достаточных сведений для адекватного определения контекста начальных данных.</span><span class="sxs-lookup"><span data-stu-id="869ab-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="869ab-138">Например, добавленный подключаемый модуль может начать получать данные пакетов от пера, который является средним.</span><span class="sxs-lookup"><span data-stu-id="869ab-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="869ab-139">Аналогично, когда подключаемый модуль удаляется во время включения объекта **RealTimeStylus** , данные подключаемого модуля, полученные подключаемым модулем, могут оказаться недостаточными для завершения обработки данных.</span><span class="sxs-lookup"><span data-stu-id="869ab-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="869ab-140">Для общей стабильности можно сбросить внутреннее состояние подключаемого модуля при вызове метода [**реалтиместилусенаблед**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) или [**реалтиместилусдисаблед**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .</span><span class="sxs-lookup"><span data-stu-id="869ab-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="869ab-141">См. также</span><span class="sxs-lookup"><span data-stu-id="869ab-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="869ab-142">Модель каскадного RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="869ab-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="869ab-143">Рекомендации по обработке ошибок для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="869ab-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="869ab-144">Данные подключаемого модуля и класс RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="869ab-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="869ab-145">Рекомендации по потокам для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="869ab-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
