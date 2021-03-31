---
description: Это приложение демонстрирует работу с классом RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Пример подключаемого модуля RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272839"
---
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="1ad15-103">Пример подключаемого модуля RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="1ad15-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="1ad15-104">Это приложение демонстрирует работу с классом [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="1ad15-105">Подробный обзор API-интерфейсов Стилусинпут, включая класс **RealTimeStylus** , см. в разделе [доступ к вводу с помощью пера и управление](accessing-and-manipulating-stylus-input.md)им.</span><span class="sxs-lookup"><span data-stu-id="1ad15-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="1ad15-106">Сведения о синхронных и асинхронных подключаемых модулях см. [в разделе подключаемые модули и класс RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="1ad15-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="1ad15-107">Общие сведения о примере</span><span class="sxs-lookup"><span data-stu-id="1ad15-107">Overview of the Sample</span></span>

<span data-ttu-id="1ad15-108">Подключаемые модули. объекты, реализующие интерфейс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) или [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , можно добавить в объект [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="1ad15-109">В этом примере приложения используется несколько типов подключаемых модулей:</span><span class="sxs-lookup"><span data-stu-id="1ad15-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="1ad15-110">Подключаемый модуль фильтра пакетов: изменяет пакеты.</span><span class="sxs-lookup"><span data-stu-id="1ad15-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="1ad15-111">Подключаемый модуль фильтра пакетов в этом примере изменяет сведения о пакете путем ограничения всех данных пакетов (x, y) в пределах прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="1ad15-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="1ad15-112">Подключаемый модуль пользовательского динамического модуля визуализации: изменяет качество динамической отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1ad15-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="1ad15-113">Настраиваемый подключаемый модуль динамической визуализации в этом примере изменяет способ отрисовки рукописных данных, рисуя небольшой кружок вокруг каждой точки (x, y) на штрихе.</span><span class="sxs-lookup"><span data-stu-id="1ad15-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="1ad15-114">Подключаемый модуль динамического рендеринга: изменяет качество динамической отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1ad15-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="1ad15-115">В этом примере демонстрируется использование объекта [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) в качестве подключаемого модуля для обработки динамической отрисовки рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="1ad15-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="1ad15-116">Подключаемый модуль распознавателя жестов: распознает жесты приложения.</span><span class="sxs-lookup"><span data-stu-id="1ad15-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="1ad15-117">В этом примере демонстрируется использование объекта [**GestureRecognizer**](gesturerecognizer-class.md) в качестве подключаемого модуля для распознавания жестов приложения (при работе в системе с присутствием распознавателя Microsoft жеста).</span><span class="sxs-lookup"><span data-stu-id="1ad15-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="1ad15-118">Кроме того, этот образец предоставляет пользовательский интерфейс, позволяющий пользователю добавлять, удалять и изменять порядок каждого подключаемого модуля в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1ad15-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="1ad15-119">Пример решения содержит два проекта: Реалтиместилусплугинапп и Реалтиместилусплугинс.</span><span class="sxs-lookup"><span data-stu-id="1ad15-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="1ad15-120">Реалтиместилусплугинапп содержит пользовательский интерфейс для примера.</span><span class="sxs-lookup"><span data-stu-id="1ad15-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="1ad15-121">Реалтиместилусплугинс содержит реализации подключаемых модулей. Проект Реалтиместилусплугинс определяет пространство имен Реалтиместилусплугинс, которое содержит фильтр пакетов и пользовательские подключаемые модули динамического рендеринга. На это пространство имен ссылается проект Реалтиместилусплугинапп.</span><span class="sxs-lookup"><span data-stu-id="1ad15-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="1ad15-122">Проект Реалтиместилусплугинс использует пространства имен [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. стилусинпут](/previous-versions/ms824750(v=msdn.10))и [Microsoft. стилусинпут. плугиндата](/previous-versions/ms823992(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="1ad15-123">Общие сведения о пространствах имен [Microsoft. стилусинпут](/previous-versions/ms824750(v=msdn.10)) и [Microsoft. стилусинпут. плугиндата](/previous-versions/ms823992(v=msdn.10)) см. в разделе [архитектура API-интерфейсов стилусинпут](architecture-of-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="1ad15-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="1ad15-124">Подключаемый модуль фильтра пакетов</span><span class="sxs-lookup"><span data-stu-id="1ad15-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="1ad15-125">Подключаемый модуль фильтра пакетов — это синхронный подключаемый модуль, демонстрирующий изменение пакетов.</span><span class="sxs-lookup"><span data-stu-id="1ad15-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="1ad15-126">В частности, он определяет прямоугольник на форме.</span><span class="sxs-lookup"><span data-stu-id="1ad15-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="1ad15-127">Все пакеты, отображаемые за пределами региона, подготавливаются к просмотру внутри региона.</span><span class="sxs-lookup"><span data-stu-id="1ad15-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="1ad15-128">Класс подключаемого модуля, `PacketFilterPlugin` , регистрируется для уведомления о `StylusDown` `StylusUp` `Packets` событиях ввода с помощью пера, и.</span><span class="sxs-lookup"><span data-stu-id="1ad15-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="1ad15-129">Класс реализует методы [стилусдовн](/previous-versions/ms824761(v=msdn.10)), [стилусуп](/previous-versions/ms824764(v=msdn.10))и [пакеты](/previous-versions/ms824756(v=msdn.10)) , определенные в классе [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="1ad15-130">Для открытого конструктора для `PacketFilterPlugin` требуется структура в виде [прямоугольника](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="1ad15-131">Этот прямоугольник определяет прямоугольную область в координатах рукописного пространства (01MM = 1 HIMETRIC Unit), в которой будут содержаться пакеты.</span><span class="sxs-lookup"><span data-stu-id="1ad15-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="1ad15-132">Прямоугольник удерживается в частном поле, `rectangle` .</span><span class="sxs-lookup"><span data-stu-id="1ad15-132">The rectangle is held in a private field, `rectangle`.</span></span>


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



<span data-ttu-id="1ad15-133">`PacketFilterPlugin`Класс регистрируется для уведомлений о событиях, реализуя метод доступа Get [](/previous-versions/ms824752(v=msdn.10)) для свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="1ad15-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="1ad15-134">В этом случае подключаемый модуль заинтересован в ответ на `StylusDown` уведомления,, `Packets` `StylusUp` и `Error` .</span><span class="sxs-lookup"><span data-stu-id="1ad15-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="1ad15-135">Этот пример возвращает эти значения, как определено в перечислении [датаинтерестмаск](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="1ad15-136">Метод [стилусдовн](/previous-versions/ms824761(v=msdn.10)) вызывается, когда кончик пера связывается с поверхностью дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="1ad15-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="1ad15-137">Метод [стилусуп](/previous-versions/ms824764(v=msdn.10)) вызывается, когда кончик пера покидает поверхность дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="1ad15-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="1ad15-138">Метод [пакетов](/previous-versions/ms824756(v=msdn.10)) вызывается, когда объект [**RealTimeStylus**](realtimestylus-class.md) получает пакеты.</span><span class="sxs-lookup"><span data-stu-id="1ad15-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="1ad15-139">Метод [Error](/previous-versions/ms585069(v=vs.100)) вызывается, когда текущий подключаемый модуль или предыдущий подключаемый модуль создает исключение.</span><span class="sxs-lookup"><span data-stu-id="1ad15-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



<span data-ttu-id="1ad15-140">`PacketFilterPlugin`Класс обрабатывает большинство этих уведомлений в вспомогательном методе `ModifyPacketData` .</span><span class="sxs-lookup"><span data-stu-id="1ad15-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="1ad15-141">`ModifyPacketData`Метод получает значения x и y для каждого нового пакета из класса [паккетсдата](/previous-versions/ms824590(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="1ad15-142">Если любое из значений находится за пределами прямоугольника, метод заменяет значение на ближайшую точку, которая по-прежнему попадает в прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="1ad15-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="1ad15-143">Это пример того, как подключаемый модуль может заменять данные пакетов по мере их получения из потока ввода с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="1ad15-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="1ad15-144">Пользовательский подключаемый модуль динамического рендеринга</span><span class="sxs-lookup"><span data-stu-id="1ad15-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="1ad15-145">`CustomDynamicRenderer`Класс также реализует класс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) для получения уведомлений, вводимых с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="1ad15-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="1ad15-146">Затем он обрабатывает `Packets` уведомление, чтобы нарисовать небольшой круг вокруг каждой новой точки пакетов.</span><span class="sxs-lookup"><span data-stu-id="1ad15-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="1ad15-147">Класс содержит [графическую](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) переменную, содержащую ссылку на объект Graphics, переданный в конструктор класса.</span><span class="sxs-lookup"><span data-stu-id="1ad15-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="1ad15-148">Это графический объект, используемый для динамической отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1ad15-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="1ad15-149">Когда подключаемый модуль пользовательского динамического модуля визуализации получает уведомление о пакетах, он извлекает данные (x, y) и рисует маленький зеленый кружок вокруг точки.</span><span class="sxs-lookup"><span data-stu-id="1ad15-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="1ad15-150">Это пример пользовательской отрисовки на основе входного потока пера.</span><span class="sxs-lookup"><span data-stu-id="1ad15-150">This is an example of custom rendering based on the pen-input stream.</span></span>


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="1ad15-151">Проект Реалтиместилусплугинапп</span><span class="sxs-lookup"><span data-stu-id="1ad15-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="1ad15-152">Проект Реалтиместилусплугинапп демонстрирует ранее описанные подключаемые модули, а также подключаемые модули [**GestureRecognizer**](gesturerecognizer-class.md) и [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . Пользовательский интерфейс проекта состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="1ad15-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="1ad15-153">Форма, содержащая элемент управления [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) , используемый для определения области рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="1ad15-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="1ad15-154">Элемент управления [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) , в котором можно вывести список и выбрать доступные подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="1ad15-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="1ad15-155">Пара [объектов Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) для включения повторного упорядочения подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="1ad15-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="1ad15-156">Проект определяет структуру, `PlugInListItem` чтобы упростить управление подключаемыми модулями, используемыми в проекте.</span><span class="sxs-lookup"><span data-stu-id="1ad15-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="1ad15-157">`PlugInListItem`Структура содержит подключаемый модуль и описание.</span><span class="sxs-lookup"><span data-stu-id="1ad15-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="1ad15-158">`RealTimeStylusPluginApp`Класс реализует класс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="1ad15-159">Это необходимо для того, чтобы `RealTimeStylusPluginApp` класс мог получать уведомления, когда подключаемый модуль [**GestureRecognizer**](gesturerecognizer-class.md) добавляет данные жестов в очередь вывода.</span><span class="sxs-lookup"><span data-stu-id="1ad15-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="1ad15-160">Приложение регистрируется для уведомления [кустомстилусдатааддед](/previous-versions/ms824753(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="1ad15-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="1ad15-161">При получении данных жеста `RealTimeStylusPluginApp` размещает его описание в строке состояния в нижней части формы.</span><span class="sxs-lookup"><span data-stu-id="1ad15-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> В реализации [кустомстилусдатааддед](/previous-versions/ms824753(v=msdn.10)) интересно, что вы можете найти данные пользовательского жеста в очереди вывода либо по GUID (с помощью поля [жестуререкогнитиондатагуид](/previous-versions/ms826344(v=msdn.10)) ), либо по типу (с помощью результата инструкции AS). В образце используются оба метода идентификации в демонстрационных целях. <span data-ttu-id="1ad15-164">Один из этих подходов также является допустимым.</span><span class="sxs-lookup"><span data-stu-id="1ad15-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="1ad15-165">В обработчике событий загрузки формы приложение создает экземпляры `PacketFilter` `CustomDynamicRenderer` классов и добавляет их в список.</span><span class="sxs-lookup"><span data-stu-id="1ad15-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="1ad15-166">Затем приложение пытается создать экземпляр класса [**GestureRecognizer**](gesturerecognizer-class.md) и, в случае успеха, добавляет его в список.</span><span class="sxs-lookup"><span data-stu-id="1ad15-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="1ad15-167">Этот сбой происходит, если распознаватель жестов отсутствует в системе.</span><span class="sxs-lookup"><span data-stu-id="1ad15-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="1ad15-168">Затем приложение создает экземпляр объекта [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) и добавляет его в список.</span><span class="sxs-lookup"><span data-stu-id="1ad15-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="1ad15-169">Наконец, приложение включает все подключаемые модули и сам объект [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad15-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="1ad15-170">Еще одно важное замечание об этом примере состоит в том, что в вспомогательных методах объект [**RealTimeStylus**](realtimestylus-class.md) сначала отключается перед добавлением или удалением подключаемых модулей, а затем снова включается после завершения добавления или удаления.</span><span class="sxs-lookup"><span data-stu-id="1ad15-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a><span data-ttu-id="1ad15-171">См. также</span><span class="sxs-lookup"><span data-stu-id="1ad15-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1ad15-172">[Microsoft. Стилусинпут. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1ad15-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="1ad15-173">[Microsoft. Стилусинпут. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1ad15-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="1ad15-174">[Microsoft. Стилусинпут. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1ad15-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="1ad15-175">[Microsoft. Стилусинпут. Датаинтерестмаск](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1ad15-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="1ad15-176">[Microsoft. Стилусинпут. Истилуссинкплугин](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1ad15-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="1ad15-177">[Microsoft. Стилусинпут. Истилусасинкплугин](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1ad15-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="1ad15-178">[Microsoft. Стилусинпут. Плугиндата. Паккетсдата](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1ad15-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="1ad15-179">Доступ к вводу пера и управление им</span><span class="sxs-lookup"><span data-stu-id="1ad15-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="1ad15-180">Подключаемые модули и класс RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="1ad15-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="1ad15-181">Пример коллекции рукописных данных RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="1ad15-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
