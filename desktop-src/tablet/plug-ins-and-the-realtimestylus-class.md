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
# <a name="plug-ins-and-the-realtimestylus-class"></a>Подключаемые модули и класс RealTimeStylus

Объект [**RealTimeStylus**](realtimestylus-class.md) предназначен для предоставления доступа к потоку данных из пера планшета в режиме реального времени. Подключаемые модули, реализующие интерфейс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) или [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , можно добавить в объект **RealTimeStylus** . Синхронные подключаемые модули, как правило, вызываются непосредственно объектом **RealTimeStylus** в потоке с высоким приоритетом, а Асинхронные подключаемые модули обычно вызываются в потоке пользовательского интерфейса приложения. Создайте или используйте синхронные подключаемые модули для задач, которым требуется доступ к потоку данных в режиме реального времени и которые не требуют вычисления, например фильтрация пакетов. Создайте или используйте асинхронные подключаемые модули для задач, не требующих доступа в режиме реального времени к потоку данных, например коллекции рукописного ввода.

Некоторые задачи могут быть требовательными к вычислительным операциям, но они требуют доступа к потоку данных в режиме реального времени, например для распознавания жестов с несколькими штрихами. Для решения этих задач интерфейсы API Стилусинпут обеспечивают каскадную модель [**RealTimeStylus**](realtimestylus-class.md) , которая позволяет использовать два объекта **RealTimeStylus** , каждый из которых выполняется в собственном потоке. Дополнительные сведения о каскадной модели **RealTimeStylus** см. в статье [каскадная модель RealTimeStylus](the-cascaded-realtimestylus-model.md).

Интерфейсы [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) и [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) определяют одни и те же методы. Эти методы позволяют объекту [**RealTimeStylus**](realtimestylus-class.md) передавать данные пера каждому подключаемому модулю независимо от того, является ли это асинхронным или синхронным подключаемым модулем. Свойства [Microsoft. стилусинпут. истилуссинкплугин.](/previous-versions/ms824752(v=msdn.10)) и [Microsoft. стилусинпут. истилусасинкплугин.](/previous-versions/ms824769(v=msdn.10)) позволяют каждому подключаемому модулю подписываться на определенные данные в потоке данных пера планшета. Подключаемый модуль должен подписываться только на данные, необходимые для выполнения задачи, минимизируя требования к производительности. Дополнительные сведения о потоках и классе **RealTimeStylus** см. в разделе [вопросы использования потоков для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md).

Объект [**RealTimeStylus**](realtimestylus-class.md) использует объекты из пространства имен [Microsoft. стилусинпут. плугиндата](/previous-versions/ms823992(v=msdn.10)) для передачи данных пера в подключаемые модули. Объект **RealTimeStylus** также перехватывает исключения, вызываемые подключаемыми модулями. Когда объект **RealTimeStylus** перехватывает исключения, он уведомляет подключаемые модули, вызывая метод [истилуссинкплугин. Error](/previous-versions/ms824754(v=msdn.10)) или [истилусасинкплугин. Error](/previous-versions/ms824771(v=msdn.10)) . Дополнительные сведения об использовании подключаемых модулей данных см. в разделе [подключаемые модули данных и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) . Дополнительные сведения об обработке ошибок см. в разделе [рекомендации по обработке ошибок для API-интерфейсов стилусинпут](error-handling-considerations-for-the-stylusinput-apis.md) и секции данных об ошибках подключаемых модулей данных и класса RealTimeStylus.

> [!Note]  
> По крайней мере один подключаемый модуль должен быть присоединен к объекту [**RealTimeStylus**](realtimestylus-class.md) , прежде чем можно будет включить объект **RealTimeStylus** .

 

В следующих разделах описаны некоторые распространенные категории подключаемых модулей.

-   [Подключаемые модули сбора рукописных данных](ink-collection-plug-ins.md)
-   [Подключаемые модули динамического рендеринга](dynamic-renderer-plug-ins.md)
-   [Подключаемые модули распознавателя](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Особые рекомендации

Из-за сложной природы объекта [**RealTimeStylus**](realtimestylus-class.md) следует обратить внимание на следующее.

Объект [**RealTimeStylus**](realtimestylus-class.md) создает исключение, если подключаемый модуль изменяет коллекцию подключаемых модулей, к которой он присоединен. Это происходит только в том случае, если подключаемый модуль делает это, пока он вызывается объектом **RealTimeStylus** как членом этой коллекции.

Следующий пример на языке C \# — это код, который заставляет объект [**RealTimeStylus**](realtimestylus-class.md) вызывать исключение.


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



Объект [**RealTimeStylus**](realtimestylus-class.md) создает исключение, если подключаемый модуль вызывает метод [Dispose](/previous-versions/ms825891(v=msdn.10)) объекта **RealTimeStylus** . Это происходит только в том случае, если подключаемый модуль делает это, пока он вызывается объектом **RealTimeStylus** .

Следующий пример на языке C \# — это код, который заставляет объект [**RealTimeStylus**](realtimestylus-class.md) вызывать исключение.


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



Коллекции подключаемых модулей можно изменить, пока включен объект [**RealTimeStylus**](realtimestylus-class.md) . Однако это может усложнить работу приложения в прогнозировании. Когда подключаемый модуль добавляется, когда объект **RealTimeStylus** включен, объект **RealTimeStylus** вызывает метод [истилусасинкплугин. реалтиместилусенаблед](/previous-versions/ms824775(v=msdn.10)) или [истилуссинкплугин. реалтиместилусенаблед](/previous-versions/ms824758(v=msdn.10)) подключаемого модуля. Когда подключаемый модуль удаляется, пока включен объект **RealTimeStylus** , объект **RealTimeStylus** вызывает метод [истилусасинкплугин. реалтиместилусдисаблед](/previous-versions/ms824774(v=msdn.10)) или [истилуссинкплугин. реалтиместилусдисаблед](/previous-versions/ms824757(v=msdn.10)) подключаемого модуля. Это позволяет подключаемому модулю поддерживать свое правильное состояние без проверки свойства [Enabled](/previous-versions/ms824832(v=msdn.10)) объекта **RealTimeStylus** .

При добавлении подключаемого модуля, когда включен объект [**RealTimeStylus**](realtimestylus-class.md) , подключаемые данные, которые получает подключаемый модуль, могут не содержать достаточных сведений для адекватного определения контекста начальных данных. Например, добавленный подключаемый модуль может начать получать данные пакетов от пера, который является средним. Аналогично, когда подключаемый модуль удаляется во время включения объекта **RealTimeStylus** , данные подключаемого модуля, полученные подключаемым модулем, могут оказаться недостаточными для завершения обработки данных.

> [!Note]  
> Для общей стабильности можно сбросить внутреннее состояние подключаемого модуля при вызове метода [**реалтиместилусенаблед**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) или [**реалтиместилусдисаблед**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модель каскадного RealTimeStylus](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Рекомендации по обработке ошибок для API-интерфейсов Стилусинпут](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Данные подключаемого модуля и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Рекомендации по потокам для API-интерфейсов Стилусинпут](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
