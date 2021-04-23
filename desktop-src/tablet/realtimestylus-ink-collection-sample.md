---
description: Это приложение демонстрирует сбор и отрисовку рукописного ввода при использовании класса RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Пример коллекции рукописных данных RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702682"
---
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="f38fa-103">Пример коллекции рукописных данных RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f38fa-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="f38fa-104">Это приложение демонстрирует сбор и отрисовку рукописного ввода при использовании класса [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="f38fa-105">Проект Инкколлектион</span><span class="sxs-lookup"><span data-stu-id="f38fa-105">The InkCollection Project</span></span>

<span data-ttu-id="f38fa-106">Этот пример состоит из одного решения, которое содержит один проект, Инкколлектион.</span><span class="sxs-lookup"><span data-stu-id="f38fa-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="f38fa-107">Приложение определяет `InkCollection` пространство имен, которое содержит один класс, также называемый `InkCollection` .</span><span class="sxs-lookup"><span data-stu-id="f38fa-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="f38fa-108">Класс наследует от класса [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) и реализует интерфейс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="f38fa-109">Класс Инкколлектион определяет набор частных констант, используемых для указания различной толщины пера.</span><span class="sxs-lookup"><span data-stu-id="f38fa-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="f38fa-110">Класс также объявляет закрытые экземпляры класса [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , класса [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` и класса модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов `myRenderer` .</span><span class="sxs-lookup"><span data-stu-id="f38fa-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="f38fa-111">**DynamicRenderer** подготавливает к просмотру [Рукописный](/previous-versions/ms552692(v=vs.100)) фрагмент, который собирается в данный момент.</span><span class="sxs-lookup"><span data-stu-id="f38fa-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="f38fa-112">Объект модуля подготовки отчетов, `myRenderer` отрисовывает объекты обводки, которые уже были собраны.</span><span class="sxs-lookup"><span data-stu-id="f38fa-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="f38fa-113">Класс также объявляет объект [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` который используется для хранения данных пакета, собираемых одним или несколькими объектами [курсора](/previous-versions/ms552104(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="f38fa-114">Значения [идентификатора](/previous-versions/ms824826(v=msdn.10)) объекта [пера](/previous-versions/ms824824(v=msdn.10)) используются в качестве ключа хэш-таблицы для уникальной идентификации данных пакета, собираемых для данного объекта курсора.</span><span class="sxs-lookup"><span data-stu-id="f38fa-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="f38fa-115">Частный экземпляр объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , `myInk` , хранящий объекты [Stroke](/previous-versions/ms552692(v=vs.100)) , собранные `myRealTimeStylus` .</span><span class="sxs-lookup"><span data-stu-id="f38fa-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="f38fa-116">Событие загрузки формы</span><span class="sxs-lookup"><span data-stu-id="f38fa-116">The Form Load Event</span></span>

<span data-ttu-id="f38fa-117">В обработчике событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) для формы создается `myDynamicRenderer` экземпляр с помощью [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , который принимает элемент управления в качестве аргумента и `myRenderer` создается с помощью конструктора без аргументов.</span><span class="sxs-lookup"><span data-stu-id="f38fa-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="f38fa-118">Обратите внимание на комментарий, который следует за созданием модулей подготовки отчетов, поскольку `myDynamicRenderer` при отрисовке рукописного ввода использует значения по умолчанию для [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="f38fa-119">Это стандартное поведение.</span><span class="sxs-lookup"><span data-stu-id="f38fa-119">This is standard behavior.</span></span> <span data-ttu-id="f38fa-120">Однако если вы хотите, чтобы рукописный текст отображался `myDynamicRenderer` иначе, чем рукописный ввод `myRenderer` , можно изменить свойство [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) в `myDynamicRenderer` .</span><span class="sxs-lookup"><span data-stu-id="f38fa-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="f38fa-121">Для этого раскомментируйте следующие строки перед сборкой и запуском приложения.</span><span class="sxs-lookup"><span data-stu-id="f38fa-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="f38fa-122">Затем приложение создает объект [**RealTimeStylus**](realtimestylus-class.md) , который используется для получения уведомлений о пере, и добавляет объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) в очередь уведомлений синхронного подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="f38fa-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="f38fa-123">В частности, `myRealTimeStylus` добавляет `myDynamicRenderer` к свойству [синкплугинколлектион](/previous-versions/ms824833(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="f38fa-124">Затем форма добавляется в очередь уведомлений асинхронного подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="f38fa-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="f38fa-125">В частности, `InkCollection` добавляется в свойство [асинкплугинколлектион](/previous-versions/ms824831(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="f38fa-126">Наконец, `myRealTimeStylus` и `myDynamicRenderer` включены, и создаются экземпляры Мипаккетс и минк.</span><span class="sxs-lookup"><span data-stu-id="f38fa-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="f38fa-127">Помимо привязки к обработчикам меню для изменения цвета и размера рукописного ввода, перед реализацией интерфейса требуется один более короткий блок кода.</span><span class="sxs-lookup"><span data-stu-id="f38fa-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="f38fa-128">Образец должен обрабатывать событие [рисования](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) формы.</span><span class="sxs-lookup"><span data-stu-id="f38fa-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="f38fa-129">В обработчике событий приложение должно быть Обновлено, `myDynamicRenderer` так как при возникновении события рисования может собираться объект [Stroke](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="f38fa-130">В этом случае необходимо перерисовать часть объекта Stroke, который уже был собран.</span><span class="sxs-lookup"><span data-stu-id="f38fa-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="f38fa-131">Статический модуль [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов используется для повторного рисования объектов Stroke, которые уже были собраны.</span><span class="sxs-lookup"><span data-stu-id="f38fa-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="f38fa-132">Эти штрихи находятся в объекте [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , так как они помещаются при рисовании, как показано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="f38fa-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="f38fa-133">Реализация интерфейса Истилусасинкплугин</span><span class="sxs-lookup"><span data-stu-id="f38fa-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="f38fa-134">Пример приложения определяет типы уведомлений, которые он получает в [качестве интереса при реализации свойства объекта](/previous-versions/ms824769(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="f38fa-135">Таким образом, свойство DataObject определяет уведомления, пересылаемые объектом [**RealTimeStylus**](realtimestylus-class.md) в форму.</span><span class="sxs-lookup"><span data-stu-id="f38fa-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="f38fa-136">В этом примере свойство **стилусдовн** определяет интерес в уведомлениях об ошибках, **пакетах**, **стилусупах** и **сообщениях ошибок** через перечисление [датаинтерестмаск](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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
```



<span data-ttu-id="f38fa-137">Уведомление [стилусдовн](/previous-versions/ms824779(v=msdn.10)) возникает, когда перо касается поверхности дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="f38fa-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="f38fa-138">В этом случае в примере выделяется массив, который используется для хранения данных пакета для объекта [пера](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="f38fa-139">[Стилусдовндата](/previous-versions/ms824107(v=msdn.10)) из метода стилусдовн добавляется в массив, а массив вставляется в хэш-таблицу с помощью свойства [идентификатора](/previous-versions/ms824826(v=msdn.10)) объекта пера в качестве ключа.</span><span class="sxs-lookup"><span data-stu-id="f38fa-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="f38fa-140">Уведомление о [пакетах](/previous-versions/ms824773(v=msdn.10)) происходит, когда перо перемещается на поверхность дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="f38fa-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="f38fa-141">В этом случае приложение добавляет новый [стилусдовндата](/previous-versions/ms824107(v=msdn.10)) в массив пакетов для объекта [пера](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f38fa-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="f38fa-142">Для этого используется свойство [идентификатора](/previous-versions/ms824826(v=msdn.10)) объекта пера в качестве ключа для получения массива пакетов для пера из хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f38fa-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="f38fa-143">После этого новые данные пакета вставляются в полученный массив.</span><span class="sxs-lookup"><span data-stu-id="f38fa-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="f38fa-144">Уведомление [стилусуп](/previous-versions/ms824782(v=msdn.10)) возникает, когда перо покидает поверхность дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="f38fa-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="f38fa-145">При появлении этого уведомления образец извлекает массив пакетов для этого объекта [пера](/previous-versions/ms824824(v=msdn.10)) из хэш-таблицы, поскольку он больше не нужен, добавляет в новые данные пакета и использует массив данных пакета для создания нового объекта [Stroke](/previous-versions/ms552692(v=vs.100)) `stroke` .</span><span class="sxs-lookup"><span data-stu-id="f38fa-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



<span data-ttu-id="f38fa-146">Пример, в котором показано более надежное использование класса [**RealTimeStylus**](realtimestylus-class.md) , включая использование пользовательского подключаемого модуля, см. [в разделе Пример подключаемого модуля RealTimeStylus](realtimestylus-plug-in-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f38fa-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f38fa-147">См. также</span><span class="sxs-lookup"><span data-stu-id="f38fa-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f38fa-148">[Microsoft. Ink. модуль подготовки отчетов](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f38fa-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="f38fa-149">[Microsoft. Стилусинпут. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f38fa-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="f38fa-150">[Microsoft. Стилусинпут. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f38fa-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="f38fa-151">[Microsoft. Стилусинпут. Истилусасинкплугин](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f38fa-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="f38fa-152">Доступ к вводу пера и управление им</span><span class="sxs-lookup"><span data-stu-id="f38fa-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
