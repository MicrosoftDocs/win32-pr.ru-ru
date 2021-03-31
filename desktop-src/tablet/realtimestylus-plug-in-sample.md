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
# <a name="realtimestylus-plug-in-sample"></a>Пример подключаемого модуля RealTimeStylus

Это приложение демонстрирует работу с классом [**RealTimeStylus**](realtimestylus-class.md) . Подробный обзор API-интерфейсов Стилусинпут, включая класс **RealTimeStylus** , см. в разделе [доступ к вводу с помощью пера и управление](accessing-and-manipulating-stylus-input.md)им. Сведения о синхронных и асинхронных подключаемых модулях см. [в разделе подключаемые модули и класс RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Общие сведения о примере

Подключаемые модули. объекты, реализующие интерфейс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) или [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , можно добавить в объект [**RealTimeStylus**](realtimestylus-class.md) . В этом примере приложения используется несколько типов подключаемых модулей:

-   Подключаемый модуль фильтра пакетов: изменяет пакеты. Подключаемый модуль фильтра пакетов в этом примере изменяет сведения о пакете путем ограничения всех данных пакетов (x, y) в пределах прямоугольной области.
-   Подключаемый модуль пользовательского динамического модуля визуализации: изменяет качество динамической отрисовки. Настраиваемый подключаемый модуль динамической визуализации в этом примере изменяет способ отрисовки рукописных данных, рисуя небольшой кружок вокруг каждой точки (x, y) на штрихе.
-   Подключаемый модуль динамического рендеринга: изменяет качество динамической отрисовки. В этом примере демонстрируется использование объекта [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) в качестве подключаемого модуля для обработки динамической отрисовки рукописного ввода.
-   Подключаемый модуль распознавателя жестов: распознает жесты приложения. В этом примере демонстрируется использование объекта [**GestureRecognizer**](gesturerecognizer-class.md) в качестве подключаемого модуля для распознавания жестов приложения (при работе в системе с присутствием распознавателя Microsoft жеста).

Кроме того, этот образец предоставляет пользовательский интерфейс, позволяющий пользователю добавлять, удалять и изменять порядок каждого подключаемого модуля в коллекции. Пример решения содержит два проекта: Реалтиместилусплугинапп и Реалтиместилусплугинс. Реалтиместилусплугинапп содержит пользовательский интерфейс для примера. Реалтиместилусплугинс содержит реализации подключаемых модулей. Проект Реалтиместилусплугинс определяет пространство имен Реалтиместилусплугинс, которое содержит фильтр пакетов и пользовательские подключаемые модули динамического рендеринга. На это пространство имен ссылается проект Реалтиместилусплугинапп. Проект Реалтиместилусплугинс использует пространства имен [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. стилусинпут](/previous-versions/ms824750(v=msdn.10))и [Microsoft. стилусинпут. плугиндата](/previous-versions/ms823992(v=msdn.10)) .

Общие сведения о пространствах имен [Microsoft. стилусинпут](/previous-versions/ms824750(v=msdn.10)) и [Microsoft. стилусинпут. плугиндата](/previous-versions/ms823992(v=msdn.10)) см. в разделе [архитектура API-интерфейсов стилусинпут](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Подключаемый модуль фильтра пакетов

Подключаемый модуль фильтра пакетов — это синхронный подключаемый модуль, демонстрирующий изменение пакетов. В частности, он определяет прямоугольник на форме. Все пакеты, отображаемые за пределами региона, подготавливаются к просмотру внутри региона. Класс подключаемого модуля, `PacketFilterPlugin` , регистрируется для уведомления о `StylusDown` `StylusUp` `Packets` событиях ввода с помощью пера, и. Класс реализует методы [стилусдовн](/previous-versions/ms824761(v=msdn.10)), [стилусуп](/previous-versions/ms824764(v=msdn.10))и [пакеты](/previous-versions/ms824756(v=msdn.10)) , определенные в классе [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .

Для открытого конструктора для `PacketFilterPlugin` требуется структура в виде [прямоугольника](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) . Этот прямоугольник определяет прямоугольную область в координатах рукописного пространства (01MM = 1 HIMETRIC Unit), в которой будут содержаться пакеты. Прямоугольник удерживается в частном поле, `rectangle` .


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



`PacketFilterPlugin`Класс регистрируется для уведомлений о событиях, реализуя метод доступа Get [](/previous-versions/ms824752(v=msdn.10)) для свойства объекта. В этом случае подключаемый модуль заинтересован в ответ на `StylusDown` уведомления,, `Packets` `StylusUp` и `Error` . Этот пример возвращает эти значения, как определено в перечислении [датаинтерестмаск](/previous-versions/ms824787(v=msdn.10)) . Метод [стилусдовн](/previous-versions/ms824761(v=msdn.10)) вызывается, когда кончик пера связывается с поверхностью дигитайзера. Метод [стилусуп](/previous-versions/ms824764(v=msdn.10)) вызывается, когда кончик пера покидает поверхность дигитайзера. Метод [пакетов](/previous-versions/ms824756(v=msdn.10)) вызывается, когда объект [**RealTimeStylus**](realtimestylus-class.md) получает пакеты. Метод [Error](/previous-versions/ms585069(v=vs.100)) вызывается, когда текущий подключаемый модуль или предыдущий подключаемый модуль создает исключение.


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



`PacketFilterPlugin`Класс обрабатывает большинство этих уведомлений в вспомогательном методе `ModifyPacketData` . `ModifyPacketData`Метод получает значения x и y для каждого нового пакета из класса [паккетсдата](/previous-versions/ms824590(v=msdn.10)) . Если любое из значений находится за пределами прямоугольника, метод заменяет значение на ближайшую точку, которая по-прежнему попадает в прямоугольник. Это пример того, как подключаемый модуль может заменять данные пакетов по мере их получения из потока ввода с помощью пера.


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



## <a name="custom-dynamic-renderer-plug-in"></a>Пользовательский подключаемый модуль динамического рендеринга

`CustomDynamicRenderer`Класс также реализует класс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) для получения уведомлений, вводимых с помощью пера. Затем он обрабатывает `Packets` уведомление, чтобы нарисовать небольшой круг вокруг каждой новой точки пакетов.

Класс содержит [графическую](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) переменную, содержащую ссылку на объект Graphics, переданный в конструктор класса. Это графический объект, используемый для динамической отрисовки.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Когда подключаемый модуль пользовательского динамического модуля визуализации получает уведомление о пакетах, он извлекает данные (x, y) и рисует маленький зеленый кружок вокруг точки. Это пример пользовательской отрисовки на основе входного потока пера.


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



## <a name="the-realtimestyluspluginapp-project"></a>Проект Реалтиместилусплугинапп

Проект Реалтиместилусплугинапп демонстрирует ранее описанные подключаемые модули, а также подключаемые модули [**GestureRecognizer**](gesturerecognizer-class.md) и [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . Пользовательский интерфейс проекта состоит из следующих компонентов:

-   Форма, содержащая элемент управления [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) , используемый для определения области рукописного ввода.
-   Элемент управления [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) , в котором можно вывести список и выбрать доступные подключаемые модули.
-   Пара [объектов Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) для включения повторного упорядочения подключаемых модулей.

Проект определяет структуру, `PlugInListItem` чтобы упростить управление подключаемыми модулями, используемыми в проекте. `PlugInListItem`Структура содержит подключаемый модуль и описание.

`RealTimeStylusPluginApp`Класс реализует класс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Это необходимо для того, чтобы `RealTimeStylusPluginApp` класс мог получать уведомления, когда подключаемый модуль [**GestureRecognizer**](gesturerecognizer-class.md) добавляет данные жестов в очередь вывода. Приложение регистрируется для уведомления [кустомстилусдатааддед](/previous-versions/ms824753(v=msdn.10)). При получении данных жеста `RealTimeStylusPluginApp` размещает его описание в строке состояния в нижней части формы.


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
> В реализации [кустомстилусдатааддед](/previous-versions/ms824753(v=msdn.10)) интересно, что вы можете найти данные пользовательского жеста в очереди вывода либо по GUID (с помощью поля [жестуререкогнитиондатагуид](/previous-versions/ms826344(v=msdn.10)) ), либо по типу (с помощью результата инструкции AS). В образце используются оба метода идентификации в демонстрационных целях. Один из этих подходов также является допустимым.

 

В обработчике событий загрузки формы приложение создает экземпляры `PacketFilter` `CustomDynamicRenderer` классов и добавляет их в список. Затем приложение пытается создать экземпляр класса [**GestureRecognizer**](gesturerecognizer-class.md) и, в случае успеха, добавляет его в список. Этот сбой происходит, если распознаватель жестов отсутствует в системе. Затем приложение создает экземпляр объекта [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) и добавляет его в список. Наконец, приложение включает все подключаемые модули и сам объект [**RealTimeStylus**](realtimestylus-class.md) .

Еще одно важное замечание об этом примере состоит в том, что в вспомогательных методах объект [**RealTimeStylus**](realtimestylus-class.md) сначала отключается перед добавлением или удалением подключаемых модулей, а затем снова включается после завершения добавления или удаления.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Microsoft. Стилусинпут. DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft. Стилусинпут. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. Датаинтерестмаск](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. Стилусинпут. Истилуссинкплугин](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. Истилусасинкплугин](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. Плугиндата. Паккетсдата](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Доступ к вводу пера и управление им](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Подключаемые модули и класс RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[Пример коллекции рукописных данных RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
