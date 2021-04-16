---
description: Следующие вопросы о потоках для планшетных ПК относятся к управляемой библиотеке.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Рекомендации по потокам управляемых библиотек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702593"
---
# <a name="managed-library-threading-considerations"></a>Рекомендации по потокам управляемых библиотек

Следующие вопросы о потоках для планшетных ПК относятся к управляемой библиотеке.

-   [Безопасность потоков](#thread-safety)
-   [Приложения STA и MTA](#sta-and-mta-applications)
-   [Windows Forms вопросы о потоках](#windows-forms-threading-considerations)
-   [Рекомендации по буферу обмена](#clipboard-considerations)
-   [Исключения в обработчиках событий](#exceptions-within-event-handlers)
-   [Удаление объектов и элементов управления](#disposing-objects-and-controls)
-   [API-интерфейсы Стилусинпут](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Классы управляемых библиотек платформы планшетных ПК обычно не являются потокобезопасными. Следующие коллекции являются потокобезопасными на уровне членов. Однако эти коллекции не гарантируют, что перечислитель защищен, если другой поток одновременно работает с коллекцией:

-   [курсорбуттонс](/previous-versions/ms839506(v=msdn.10))
-   [Курсоры](/previous-versions/ms839493(v=msdn.10))
-   [дивисионунитс](/previous-versions/ms837954(v=msdn.10))
-   [рекогнитионалтернатес](/previous-versions/ms830115(v=msdn.10))
-   [Распознаватели](/previous-versions/ms828520(v=msdn.10))
-   [Планшеты](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Приложения STA и MTA

Управляемые приложения, созданные с помощью мастеров, содержащихся в Microsoft Visual Studio .NET, по умолчанию являются однопотоковыми апартаментами (STA). Вы можете изменить подразделение приложения, задав для потока STA или атрибута потока многопотокового подразделения (MTA) точку входа приложения.

Если приложение выполняется в MTA, необходимо написать потокобезопасный код. Тем не менее, это позволяет повысить производительность обработки определенных событий.

Дополнительные сведения об атрибутах потоков STA и MTA см. в разделе класс [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) и класс [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .

## <a name="windows-forms-threading-considerations"></a>Windows Forms вопросы о потоках

Элементы управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) и [InkEdit](/previous-versions/ms552265(v=vs.100)) расширяют элементы управления Windows Forms. Windows Forms элементы управления используют модель однопотокового подразделения (STA), поскольку Windows Forms основаны на собственных окнах Win32, которые по сути являются отдельными потоками. В управляемом коде элементы управления рукописного ввода должны создаваться в том же потоке, что и основной поток для формы.

В приложении STA определенные события происходят в потоке, отличном от потока пользовательского интерфейса приложения. При вызове любого Windows Forms объекта или элемента управления, включая элементы управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) и [InkEdit](/previous-versions/ms552265(v=vs.100)) , из обработчика событий планшетного ПК используйте наследуемый метод [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) объекта или элемента управления. Свойство [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , унаследованное от класса Control, может использоваться для определения необходимости.

Например, в следующем обработчике события для события [распознавания](/previous-versions/ms829424(v=msdn.10)) проверяется свойство [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , а при **значении true** обработчик событий вызывается повторно из потока пользовательского интерфейса.


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



Если вы поместили элемент [управления UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) на авебпажеин браузере (см. раздел [веб-элементы управления](web-controls.md)), он выполняется как приложение STA. Для интеллектуальных клиентских приложений (см. раздел [без сенсорного развертывания](no-touch-deployment.md)) разработчик имеет полный контроль над [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). (По умолчанию обычно используется STA, но в зависимости от используемой версии среды CLR это может быть MTA.) О проблемах с потоками, связанных с [**RealTimeStylus**](realtimestylus-class.md), см. [в разделе вопросы многопоточности для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md).

Дополнительные сведения о вызове Windows Forms из приложения MTA см. в разделе [Пример многопоточного Windows Forms управления](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Рекомендации по буферу обмена

Объект [Clipboard](../dataxchg/clipboard.md) работает только из потока STA. При попытке скопировать или вставить из буфера обмена из потока, который не является STA, вы получаете [среадстатиксцептион](/previous-versions/windows/). Если приложение является MTA, создайте поток STA для обработки вызовов методов буфера обмена и некоторых других аспектов пользовательского интерфейса приложения.

## <a name="exceptions-within-event-handlers"></a>Исключения в обработчиках событий

Исключения не могут быть вызваны в обработчиках событий планшетных ПК. Например, если делегат обработчика событий для объекта или коллекции Tablet PC имеет три зарегистрированных обработчика, а первый — исключение, то происходит следующая последовательность.

1.  Первый обработчик завершает работу.
2.  Исключение потеряно.
3.  Остальные обработчики не вызываются.

## <a name="disposing-objects-and-controls"></a>Удаление объектов и элементов управления

Чтобы избежать утечки памяти, необходимо явно вызвать метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) для любого объекта или элемента управления Tablet PC, к которому был присоединен обработчик событий до того, как объект или элемент управления выходит из области действия.

Чтобы повысить производительность приложения, вручную удалите любой объект или элемент управления Tablet PC, реализующий метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) , когда объект или элемент управления больше не нужен.

## <a name="stylusinput-apis"></a>API-интерфейсы Стилусинпут

Дополнительные сведения о создании потоков для объекта [**RealTimeStylus**](realtimestylus-class.md) и интерфейсов прикладного программирования (API) стилусинпут см. [в статье вопросы использования потоков для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md).

 

 
