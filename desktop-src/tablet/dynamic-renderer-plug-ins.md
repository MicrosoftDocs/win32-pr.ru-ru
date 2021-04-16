---
description: Подключаемый модуль динамического рендеринга — это объект, который отображает данные пера планшета в режиме реального времени по мере его обработки объектом RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Подключаемые модули Dynamic-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c3f1a33c3cd7faef2e899bcb198ea64aa5bd76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551866"
---
# <a name="dynamic-renderer-plug-ins"></a>Подключаемые модули Dynamic-Renderer

Подключаемый модуль динамического рендеринга — это объект, который отображает данные пера планшета в режиме реального времени по мере его обработки объектом [**RealTimeStylus**](realtimestylus-class.md) . В дальнейшем для таких событий, как обновление формы, подключаемый модуль динамического рендеринга или подключаемый модуль сборщика рукописных данных может перерисовывать рукописный ввод.

## <a name="the-dynamicrenderer-object"></a>Объект DynamicRenderer

Объект [**RealTimeStylus**](realtimestylus-class.md) реализует интерфейс [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) визуализирует рукописный ввод в режиме реального времени по мере его прорисовки. Когда метод [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) вызывается, когда включен объект **DynamicRenderer** , объект **DynamicRenderer** перерисовывает собранный в данный момент росчерк. Свойство [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) объекта **DynamicRenderer** изначально имеет значение **false**.

> [!Note]  
> При вызове метода [**Refresh**](/previous-versions/ms826370(v=msdn.10)) объекта [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) из обработчика событий [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) в управляемом коде установите свойство [**Клипректангле**](/previous-versions/ms826346(v=msdn.10)) объекта **DynamicRenderer** в свойство [клипректангле](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) объекта [PaintEventArgs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) .

 

Объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) может временно кэшировать данные рукописного ввода. Чтобы использовать эту функцию в управляемом коде, установите для свойства [енабледатакаче](/previous-versions/ms826349(v=msdn.10)) значение **true**. Когда объект [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) получает вызов своего метода [**истилуссинкплугин. стилусуп**](/previous-versions/ms826366(v=msdn.10)) , он кэширует данные Stroke и добавляет пользовательские данные пера во входную очередь в ответ на объект [**стилусупдата**](/previous-versions/ms824057(v=msdn.10)) для штриха. Свойству [кустомдатаид](/previous-versions/ms824749(v=msdn.10)) объекта [**кустомстилусдата**](/previous-versions/ms824747(v=msdn.10)) присвоено значение [динамикрендереркачеддатагуид](/previous-versions/ms824744(v=msdn.10)) , а свойство данных объекта **кустомстилусдата** содержит объект динамикрендереркачеддата. Вызовите метод [релеасекачеддата](/previous-versions/ms826371(v=msdn.10)) объекта **DynamicRenderer** после сбора штриха и его отображения в статическом виде. При вызове метода [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) , когда включен объект **DynamicRenderer** , объект **DynamicRenderer** перерисовывает все росчерки, которые кэшируются. Если свойство [**датакачинаблед**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) имеет значение **false**, кэшированные данные Stroke удаляются.

На следующей схеме показано, как объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) добавляет данные в данные пера планшета, когда задано свойство [**датакачинаблед**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) объекта **DynamicRenderer** .

![Иллюстрация, демонстрирующая поток данных DynamicRenderer](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

На этой схеме круг с буквой "SD" представляет объект [**стилусдовн**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) , а круг букв "P" — объекты [**пакетов**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) , которые уже добавлены в очередь вывода объекта [**RealTimeStylus**](realtimestylus-class.md) и которые еще не были отправлены в асинхронную коллекцию подключаемых модулей. Кружок с буквой "SU" представляет объект [**стилусуп**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) , который в настоящее время обрабатывается объектом **RealTimeStylus** . Он отправляется в коллекцию синхронных подключаемых модулей, а затем помещается в очередь вывода. Круги с буквами "DR" представляют пользовательские данные пера, которые добавляются во входную очередь подключаемым модулем [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) в ответ на уведомление о создании пера, связанное с "su". Пользовательское перо с буквой «DR» затем передается в синхронные подключаемые модули, а затем в очередь вывода до обработки следующих данных пера планшета. Пустой кружок представляет позицию в очереди вывода, в которой добавляются будущие данные пера планшета. Кроме того, на схеме представлен подключаемый модуль, вызывающий метод [**релеасекачеддата**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) объекта **DynamicRenderer** для освобождения кэшированных данных Stroke после того, как подключаемый модуль коллекции рукописного ввода обработал штрих.

### <a name="special-considerations"></a>Особые рекомендации

В следующем списке приводятся другие моменты, которые следует учитывать при использовании объекта [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) .

-   Не следует присоединять объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) к более чем одному объекту [**RealTimeStylus**](realtimestylus-class.md) . После включения двух объектов **RealTimeStylus** , к которым присоединен объект **DynamicRenderer** , происходит следующее.

    -   Объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) создает исключение в ответ на второй вызов его метода [**реалтиместилусенаблед**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) .
    -   Второй объект [**RealTimeStylus**](realtimestylus-class.md) , который был включен, создает объект [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) и уведомляет остальные подключаемые модули в своих коллекциях подключаемых модулей ошибки.
    -   Объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) останавливает отрисовку данных пера планшета.

-   Объект [**RealTimeStylus**](realtimestylus-class.md) создает исключение при вызове метода [**аддкустомстилусдататокуеуе**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) с параметром *GUID* , равным глобальному уникальному идентификатору (GUID) динамикрендереркачеддатагуид.
-   Объект [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) реализуется как оболочка модели COM, и вы не можете напрямую вызывать его методы интерфейса [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Дополнительные сведения об операциях COM и объекте [**RealTimeStylus**](realtimestylus-class.md) см. [в разделе Примечания по реализации для API-интерфейсов стилусинпут](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Пользовательская отрисовка

Вы можете создать собственный подключаемый модуль динамического рендеринга, создав синхронный подключаемый модуль, который подписывается на уведомления [**стилусдовн**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**пакеты**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)и [**стилусуп**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) . Подключаемый модуль может затем отображать штрих при его прорисовке. Это может быть одним из способов реализации инструмента выбора, который использует Выделение произвольной формы или поле выбора, например.

 

 
