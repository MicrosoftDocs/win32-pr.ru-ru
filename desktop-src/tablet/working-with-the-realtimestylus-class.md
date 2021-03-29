---
description: Класс RealTimeStylus является частью Стилусинпут прикладных программных интерфейсов (API). В следующих разделах описываются ключевые элементы класса RealTimeStylus и интерфейсов API Стилусинпут.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Работа с классом RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 919c4de38cb0835996928c877ca4c42faf6a5f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810474"
---
# <a name="working-with-the-realtimestylus-class"></a>Работа с классом RealTimeStylus

Класс [**RealTimeStylus**](realtimestylus-class.md) является частью стилусинпут прикладных программных интерфейсов (API). В следующих разделах описываются ключевые элементы класса **RealTimeStylus** и интерфейсов API стилусинпут.

## <a name="instantiating-the-realtimestylus-class"></a>Создание экземпляра класса RealTimeStylus

При создании объекта [**RealTimeStylus**](realtimestylus-class.md) у вас есть возможность присоединить его к обработчику окна или элементу управления. Для присоединения объекта **RealTimeStylus** к обработчику окна требуются дополнительные разрешения. Дополнительные сведения об этих разрешениях см. [в разделе рекомендации по частичному доверию для API-интерфейсов стилусинпут](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> Невозможно присоединить объект [**RealTimeStylus**](realtimestylus-class.md) к окну или элементу управления в другом процессе.

 

При использовании конструктора по умолчанию создается объект [**RealTimeStylus**](realtimestylus-class.md) , который может принимать только входные данные другого объекта **RealTimeStylus** . Дополнительные сведения о соединении двух объектов **RealTimeStylus** см. [в статье каскадная модель RealTimeStylus](the-cascaded-realtimestylus-model.md).

Объект [**RealTimeStylus**](realtimestylus-class.md) реализует интерфейс [IDisposable](/dotnet/api/system.idisposable) .

## <a name="extending-the-realtimestylus-class"></a>Расширение класса RealTimeStylus

Чтобы разрешить подключаемым модулям взаимодействовать с потоком данных с помощью пера планшета, объект [**RealTimeStylus**](realtimestylus-class.md) поддерживает две подключаемые коллекции, доступные [**Жетстилуссинкплугин**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) и методы [**Жетстилусасинкплугин**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) в C++ и свойства [синкплугинколлектион](/previous-versions/ms824833(v=msdn.10)) и [асинкплугинколлектион](/previous-versions/ms824831(v=msdn.10)) в управляемом коде. Подключаемый модуль можно добавить, вызвав метод [**аддстилуссинкплугин**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) или [**аддстилусасинкплугин**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) коллекции в соответствующем свойстве. Дополнительные сведения о создании и использовании подключаемых модулей см. [в разделе подключаемые модули и класс RealTimeStylus](plug-ins-and-the-realtimestylus-class.md). Сведения о принятии решения о создании синхронного или асинхронного подключаемого модуля для конкретной задачи см. в разделе [вопросы работы с потоками для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md) и [рекомендации по производительности для API-интерфейсов стилусинпут](performance-considerations-for-the-stylusinput-apis.md).

Синхронные подключаемые модули должны реализовывать интерфейс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) , а Асинхронные подключаемые модули должны реализовывать интерфейс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . У каждого подключаемого модуля есть свойство [**истилуссинкплугин. увлечение**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) или [**истилусасинкплугин.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) объект. Объект [**RealTimeStylus**](realtimestylus-class.md) вызывает только методы уведомления подключаемого модуля для методов, на которые подписан подключаемый модуль. Дополнительные сведения о методах уведомления см. в разделе [данные подключаемого модуля и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Объект [**RealTimeStylus**](realtimestylus-class.md) реализует интерфейс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Единственный способ создать экземпляр объекта **RealTimeStylus** , который принимает входные данные из другого объекта **RealTimeStylus** , — использовать конструктор по умолчанию и реализовать каскадную модель **RealTimeStylus** . Дополнительные сведения о соединении двух объектов **RealTimeStylus** см. [в каскадной модели RealTimeStylus](the-cascaded-realtimestylus-model.md).

Объект [**RealTimeStylus**](realtimestylus-class.md) содержит две внутренние очереди, которые содержат данные пера планшета, очередь ввода и выходную очередь. Данные пера преобразуются в экземпляры классов в пространстве имен [Microsoft. стилусинпут. плугиндата](/previous-versions/ms574862(v=vs.100)) . В следующем списке описано, как объект **RealTimeStylus** обрабатывает данные пера планшета.

1.  Объект [**RealTimeStylus**](realtimestylus-class.md) сначала проверяет объекты подключаемых модулей данных во входной очереди, а затем из потока данных пера планшета.
2.  Объект [**RealTimeStylus**](realtimestylus-class.md) отправляет один объект подключаемых данных в объекты в его синхронной коллекции подключаемых модулей. Каждый синхронный подключаемый модуль может добавлять данные в очередь ввода или вывода.
3.  После отправки объекта данных подключаемого модуля всем членам коллекции синхронного подключаемого модуля объект данных подключаемого модуля помещается в очередь вывода объекта [**RealTimeStylus**](realtimestylus-class.md) .
4.  Затем объект [**RealTimeStylus**](realtimestylus-class.md) проверяет для обработки следующий объект данных подключаемого модуля.
5.  Хотя очередь вывода объекта [**RealTimeStylus**](realtimestylus-class.md) содержит данные, объект **RealTimeStylus** отправляет один объект подключаемых данных из своей очереди вывода в объекты в его асинхронной коллекции подключаемых модулей. Каждый асинхронный подключаемый модуль может добавлять данные в очередь ввода или вывода, но так как асинхронные подключаемые модули выполняются в потоке пользовательского интерфейса, данные добавляются в очередь относительно текущих данных пера, обрабатываемых объектом **RealTimeStylus** , а не относительно данных, обрабатываемых асинхронным подключаемым модулем.

На следующей схеме показан поток данных пера планшета через объект [**RealTimeStylus**](realtimestylus-class.md) и коллекции подключаемых модулей.

![иллустратиом, демонстрирующий поток данных пера планшетного ПК](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

На этой диаграмме круги с буквами "A" и "B" представляют данные пера планшета, которые уже добавлены в выходную очередь объекта [**RealTimeStylus**](realtimestylus-class.md) и еще не были отправлены в асинхронную коллекцию подключаемых модулей. Кружок с буквой "C" представляет данные пера планшета, обрабатываемые объектом **RealTimeStylus** в данный момент. Он отправляется в коллекцию синхронных подключаемых модулей и помещается в очередь вывода. Пустой кружок представляет позицию в очереди вывода, в которой добавляются будущие данные пера планшета.

Дополнительные сведения о том, как конкретные данные добавляются в очередь и обрабатываются, см. [в разделе данные подключаемого модуля и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Ниже приведен минимальный сценарий использования объекта [**RealTimeStylus**](realtimestylus-class.md) в форме, собирающей рукописный ввод.

1.  Создайте форму, реализующую интерфейс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Создайте объект [**RealTimeStylus**](realtimestylus-class.md) , присоединенный к элементу управления в форме.
3.  Задайте интерес в уведомлениях Стилусдовн, пакеты и Стилусуп в свойстве [**истилусасинкплугин.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) объект формы.
4.  В методах [**стилусдовн**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**пакетов**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)и [**стилусуп**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) формы добавьте код для управления уведомлениями о нажатии пера, пакетами и отправкой пера, которые отправляются из объекта [**RealTimeStylus**](realtimestylus-class.md) формы.

Пример такого приложения см. в разделе [образец рукописного сбора RealTimeStylus](realtimestylus-ink-collection-sample.md).

## <a name="working-with-tablet-objects"></a>Работа с объектами планшета

Каждый включенный объект [**RealTimeStylus**](realtimestylus-class.md) поддерживает список уникальных идентификаторов для объектов [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) , с которыми он может взаимодействовать. Объект **RealTimeStylus** предоставляет два метода для преобразования между уникальным идентификатором и объектом **планшета** : методами [**жеттаблетконтекстидфромтаблет**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) и [**жеттаблетфромтаблетконтекстид**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid) .

Объект [таблетпропертидескриптион](/previous-versions/ms827769(v=msdn.10)) (в управляемом коде) содержит свойство [Паккетпропертид](/previous-versions/ms827780(v=msdn.10)) и структуру [таблетпропертиметрикс](/previous-versions/ms827781(v=msdn.10)) , описывающую диапазон, разрешение и единицы свойства для конкретного объекта [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Метод [**жетдесиредпаккетдескриптион**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) объекта [**RealTimeStylus**](realtimestylus-class.md) возвращает массив глобальных уникальных идентификаторов (GUID) для свойств пакета, которые объект **RealTimeStylus** перенаправляет в свои подключаемые модули, если эти свойства пакетов доступны. Чтобы изменить набор свойств пакета, который объект **RealTimeStylus** передает в свои подключаемые модули, вызовите метод [**сетдесиредпаккетдескриптион**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) объекта **RealTimeStylus** . Метод [жеттаблетпропертидескриптионколлектион](/previous-versions/ms825935(v=msdn.10)) (в управляемом коде) объекта **RealTimeStylus** принимает уникальный идентификатор планшета и возвращает коллекцию объектов [таблетпропертидескриптион](/previous-versions/ms827760(v=msdn.10)) . Эти свойства пакетов представляют подмножество свойств, поддерживаемых планшетом, возвращаемых методом **жетдесиредпаккетдескриптион** .

Список идентификаторов GUID стандартных свойств пакетов см. в разделе класс [констант паккетпропертигуидс](packetpropertyguids-constants.md) .

## <a name="special-considerations"></a>Особые рекомендации

В следующем списке описываются другие моменты, которые следует учитывать при использовании объекта [**RealTimeStylus**](realtimestylus-class.md) с объектом [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

-   Метод [**сетдесиредпаккетдескриптион**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) может быть вызван только при отключенном объекте [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Объект [**RealTimeStylus**](realtimestylus-class.md) может изменять список требуемых свойств пакетов. Поэтому вызовите метод [**жетдесиредпаккетдескриптион**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) после вызова метода **сетдесиредпаккетдескриптион** , чтобы определить, какие свойства пакетов объект **RealTimeStylus** может пересылать в свои подключаемые модули. Планшетный ПК гарантирует поддержку значений **X**, **Y** и **паккетстатус** для [паккетпроперти](packetproperty-guids.md). Таким образом, при проектировании подключаемого модуля может потребоваться получение меньшего количества свойств пакета, чем требуется.
-   Метод [жеттаблетпропертидескриптионколлектион](/previous-versions/ms825935(v=msdn.10)) (для управляемого кода) может быть вызван только тогда, когда включен объект [**RealTimeStylus**](realtimestylus-class.md) . Так как уведомление может быть отправлено в асинхронные подключаемые модули после отключения объекта **RealTimeStylus** , может потребоваться кэшировать сведения для каждого объекта [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Метод Жеттаблетпропертидескриптионколлектион возвращает список требуемых свойств пакетов, которые поддерживаются указанным планшетом.
-   Когда объект [**RealTimeStylus**](realtimestylus-class.md) включен, каждый подключаемый модуль получает вызов своего метода [**реалтиместилусенаблед**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) . Объект [реалтиместилусенабледдата](/previous-versions/ms824229(v=msdn.10)) , переданный в уведомлении, содержит коллекцию идентификаторов контекста для доступных планшетов во время включения объекта **RealTimeStylus** .
-   Когда планшет, который может использоваться объектом [**RealTimeStylus**](realtimestylus-class.md) , добавляется на планшетный ПК или удаляется с него, пока включен объект **RealTimeStylus** , объект **RealTimeStylus** уведомляет свои подключаемые модули о добавлении или удалении объекта [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Дополнительные сведения см. в разделе [подключаемые данные и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Работа с перьями планшета

Объект [**RealTimeStylus**](realtimestylus-class.md) передает сведения о планшетном пере в свои подключаемые модули в ряде методов уведомления. Сведения о планшетном пере представлены объектом [пера](/previous-versions/ms824824(v=msdn.10)) , полученным с помощью метода [**пере**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) . Этот объект представляет собой представление пера планшета на момент сбора данных. Так как подключаемые модули получают данные пера планшета как часть потока данных пера планшета, подключаемые модули должны использовать информацию в объекте Pen, а не проверять текущее состояние определенного пера планшета с помощью класса [**курсора**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Сведения о том, как перо планшета и кнопки пера планшета передаются в подключаемые модули, см. [в разделе данные подключаемого модуля и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Чтобы получить массив объектов [пера](/previous-versions/ms824824(v=msdn.10)) , обнаруженных объектом [**RealTimeStylus**](realtimestylus-class.md) с момента последнего включения, используйте метод « [**пера**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) » объекта **RealTimeStylus** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Microsoft. Ink. планшет](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. Стилусинпут. RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[Модель каскадного RealTimeStylus](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Рекомендации по частичному доверию для API-интерфейсов Стилусинпут](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Данные подключаемого модуля и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Рекомендации по потокам для API-интерфейсов Стилусинпут](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
