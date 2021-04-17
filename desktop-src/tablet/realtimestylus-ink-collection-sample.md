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
# <a name="realtimestylus-ink-collection-sample"></a>Пример коллекции рукописных данных RealTimeStylus

Это приложение демонстрирует сбор и отрисовку рукописного ввода при использовании класса [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="the-inkcollection-project"></a>Проект Инкколлектион

Этот пример состоит из одного решения, которое содержит один проект, Инкколлектион. Приложение определяет `InkCollection` пространство имен, которое содержит один класс, также называемый `InkCollection` . Класс наследует от класса [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) и реализует интерфейс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



Класс Инкколлектион определяет набор частных констант, используемых для указания различной толщины пера. Класс также объявляет закрытые экземпляры класса [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , класса [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` и класса модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов `myRenderer` . **DynamicRenderer** подготавливает к просмотру [Рукописный](/previous-versions/ms552692(v=vs.100)) фрагмент, который собирается в данный момент. Объект модуля подготовки отчетов, `myRenderer` отрисовывает объекты обводки, которые уже были собраны.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



Класс также объявляет объект [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` который используется для хранения данных пакета, собираемых одним или несколькими объектами [курсора](/previous-versions/ms552104(v=vs.100)) . Значения [идентификатора](/previous-versions/ms824826(v=msdn.10)) объекта [пера](/previous-versions/ms824824(v=msdn.10)) используются в качестве ключа хэш-таблицы для уникальной идентификации данных пакета, собираемых для данного объекта курсора.

Частный экземпляр объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , `myInk` , хранящий объекты [Stroke](/previous-versions/ms552692(v=vs.100)) , собранные `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>Событие загрузки формы

В обработчике событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) для формы создается `myDynamicRenderer` экземпляр с помощью [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , который принимает элемент управления в качестве аргумента и `myRenderer` создается с помощью конструктора без аргументов.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Обратите внимание на комментарий, который следует за созданием модулей подготовки отчетов, поскольку `myDynamicRenderer` при отрисовке рукописного ввода использует значения по умолчанию для [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) . Это стандартное поведение. Однако если вы хотите, чтобы рукописный текст отображался `myDynamicRenderer` иначе, чем рукописный ввод `myRenderer` , можно изменить свойство [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) в `myDynamicRenderer` . Для этого раскомментируйте следующие строки перед сборкой и запуском приложения.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



Затем приложение создает объект [**RealTimeStylus**](realtimestylus-class.md) , который используется для получения уведомлений о пере, и добавляет объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) в очередь уведомлений синхронного подключаемого модуля. В частности, `myRealTimeStylus` добавляет `myDynamicRenderer` к свойству [синкплугинколлектион](/previous-versions/ms824833(v=msdn.10)) .


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



Затем форма добавляется в очередь уведомлений асинхронного подключаемого модуля. В частности, `InkCollection` добавляется в свойство [асинкплугинколлектион](/previous-versions/ms824831(v=msdn.10)) . Наконец, `myRealTimeStylus` и `myDynamicRenderer` включены, и создаются экземпляры Мипаккетс и минк.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Помимо привязки к обработчикам меню для изменения цвета и размера рукописного ввода, перед реализацией интерфейса требуется один более короткий блок кода. Образец должен обрабатывать событие [рисования](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) формы. В обработчике событий приложение должно быть Обновлено, `myDynamicRenderer` так как при возникновении события рисования может собираться объект [Stroke](/previous-versions/ms552692(v=vs.100)) . В этом случае необходимо перерисовать часть объекта Stroke, который уже был собран. Статический модуль [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов используется для повторного рисования объектов Stroke, которые уже были собраны. Эти штрихи находятся в объекте [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , так как они помещаются при рисовании, как показано в следующем разделе.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Реализация интерфейса Истилусасинкплугин

Пример приложения определяет типы уведомлений, которые он получает в [качестве интереса при реализации свойства объекта](/previous-versions/ms824769(v=msdn.10)) . Таким образом, свойство DataObject определяет уведомления, пересылаемые объектом [**RealTimeStylus**](realtimestylus-class.md) в форму. В этом примере свойство **стилусдовн** определяет интерес в уведомлениях об ошибках, **пакетах**, **стилусупах** и **сообщениях ошибок** через перечисление [датаинтерестмаск](/previous-versions/ms824787(v=msdn.10)) .


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



Уведомление [стилусдовн](/previous-versions/ms824779(v=msdn.10)) возникает, когда перо касается поверхности дигитайзера. В этом случае в примере выделяется массив, который используется для хранения данных пакета для объекта [пера](/previous-versions/ms824824(v=msdn.10)) . [Стилусдовндата](/previous-versions/ms824107(v=msdn.10)) из метода стилусдовн добавляется в массив, а массив вставляется в хэш-таблицу с помощью свойства [идентификатора](/previous-versions/ms824826(v=msdn.10)) объекта пера в качестве ключа.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



Уведомление о [пакетах](/previous-versions/ms824773(v=msdn.10)) происходит, когда перо перемещается на поверхность дигитайзера. В этом случае приложение добавляет новый [стилусдовндата](/previous-versions/ms824107(v=msdn.10)) в массив пакетов для объекта [пера](/previous-versions/ms824824(v=msdn.10)) . Для этого используется свойство [идентификатора](/previous-versions/ms824826(v=msdn.10)) объекта пера в качестве ключа для получения массива пакетов для пера из хэш-таблицы. После этого новые данные пакета вставляются в полученный массив.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



Уведомление [стилусуп](/previous-versions/ms824782(v=msdn.10)) возникает, когда перо покидает поверхность дигитайзера. При появлении этого уведомления образец извлекает массив пакетов для этого объекта [пера](/previous-versions/ms824824(v=msdn.10)) из хэш-таблицы, поскольку он больше не нужен, добавляет в новые данные пакета и использует массив данных пакета для создания нового объекта [Stroke](/previous-versions/ms552692(v=vs.100)) `stroke` .


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



Пример, в котором показано более надежное использование класса [**RealTimeStylus**](realtimestylus-class.md) , включая использование пользовательского подключаемого модуля, см. [в разделе Пример подключаемого модуля RealTimeStylus](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Microsoft. Ink. модуль подготовки отчетов](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft. Стилусинпут. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. Истилусасинкплугин](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Доступ к вводу пера и управление им](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
