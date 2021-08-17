---
description: Общие сведения о общих вопросах многопоточности.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Общие рекомендации по потокам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092578"
---
# <a name="general-threading-considerations"></a>Общие рекомендации по потокам

Ниже приведены общие рекомендации по работе с потоками при разработке для планшетных ПК.

-   [Приложения и потоки, не относящиеся к приложениям](#application-and-non-application-threads)
-   [Вопросы производительности](#performance-considerations)
    -   [Обработчики событий](#event-handlers)
    -   [Ауторедрав, свойство](#autoredraw-property)
    -   [Динамикрендеринг, свойство](#dynamicrendering-property)
-   [Рекомендации по потокам событий](#event-threading-considerations)
    -   [События объектов InkCollector и InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [События сбора рукописных объектов и штрихов](#ink-object-and-strokes-collection-events)
    -   [События распознавания](#recognition-events)
    -   [События панели ввода пера](#pen-input-panel-events)
-   [Связанные темы](#related-topics)

## <a name="application-and-non-application-threads"></a>Приложения и потоки, не относящиеся к приложениям

Все события рукописного ввода создаются в отдельном потоке рукописного ввода с высоким приоритетом. Это позволяет работать с рукописным вводом плавно, даже если приложение работает медленно. Однако обработчики событий могут замедлить работу или заблокировать отрисовку рукописного ввода.

Все события распознавания, создаваемые вызовами метода распознавания фона, обрабатываются в отдельном потоке фонового распознавания текста с нормальным приоритетом.

Все события мыши создаются в основном потоке пользовательского интерфейса приложения.

## <a name="performance-considerations"></a>Вопросы производительности

### <a name="event-handlers"></a>Обработчики событий

Прикладной программный интерфейс (API) платформы Tablet PC имеет интерактивную модель для событий, а не для модели уведомления. Не заключайте код в обработчики событий, чтобы сократить время блокировки отрисовки рукописных данных. Набор рукописных данных Tablet PC не блокируется, но приложение не получает рукописный ввод, пока приложение заблокировано.

### <a name="autoredraw-property"></a>Ауторедрав, свойство

Когда приложение выполняет пользовательскую отрисовку или если ваше приложение чувствительно к проблемам рисования, можно выполнить перерисовку самостоятельно и установить свойство [**ауторедрав**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) в **значение false** для объекта [**InkCollector**](inkcollector-class.md) , объекта [**InkOverlay**](inkoverlay-class.md) или элемента управления [InkPicture](inkpicture-control.md) . Используйте события, приведенные в следующей таблице, для управления перерисовкой.



| Объект или элемент управления                                            | Событие                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Объектами<br/> | элемент управления базового элемента управления [. недействительные](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) и события [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Объектами<br/>     | элемент управления базового элемента управления [. недействительные](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) и события [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/>                                 |
| [InkPicture](inkpicture-control.md) Элемента<br/>      | элементы управления, наследуемые элементом управления [InkPicture](inkpicture-control.md) [. недействительны](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) и события [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/> |



 

### <a name="dynamicrendering-property"></a>Динамикрендеринг, свойство

Когда приложение выполняет пользовательскую отрисовку или требуется, чтобы информация, но не рукописный ввод, можно было самостоятельно обменять и отключать отрисовку рукописного ввода в режиме реального времени, присвоив свойству [**динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) **значение false** для объекта [**InkCollector**](inkcollector-class.md) , объекта [**InkOverlay**](inkoverlay-class.md) или элемента управления [InkPicture](inkpicture-control.md) .

## <a name="event-threading-considerations"></a>Рекомендации по потокам событий

События API платформы планшетных ПК вызываются в различных потоках.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>События объектов InkCollector и InkOverlay

Большинство событий объекта [**InkCollector**](inkcollector-class.md) и [**InkOverlay**](inkoverlay-class.md) вызываются в потоке рукописного ввода. В потоке пользовательского интерфейса вызываются только события мыши для этих объектов. Например, для объекта **InkCollector** в ПОТОКЕ пользовательского интерфейса возникает событие [**MouseDown**](inkcollector-mousedown.md) , а в потоке рукописного ввода возникает событие [**курсордовн**](inkcollector-cursordown.md) .

### <a name="ink-object-and-strokes-collection-events"></a>События сбора рукописных объектов и штрихов

События [**рукописного ввода**](inkdisp-class.md) и сбора [**штрихов**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) могут поступать из потока рукописного ввода или из потока пользовательского интерфейса. Когда приложение манипулирует объектом **рукописного ввода** или коллекцией **штрихов** , событие создается в потоке пользовательского интерфейса. Когда объект [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) обновляет коллекцию объектов **Ink** или **Stroke** , событие создается в потоке рукописного ввода.

Элементы управления [InkPicture](inkpicture-control-reference.md) и [InkEdit](inkedit-control-reference.md) работают в однопотоковом подразделении (STA). Когда элемент управления InkPicture или InkEdit обновляет коллекцию объектов [**рукописного ввода**](inkdisp-class.md) или [**штрихов**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , в потоке пользовательского интерфейса возникает событие.

### <a name="recognition-events"></a>События распознавания

События распознавания вызываются в потоке пользовательского интерфейса или в потоке распознавания фона.

-   Метод [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) элемента управления [InkEdit](inkedit-control-reference.md) вызывает событие [распознавания](/previous-versions/ms836436(v=msdn.10)) (только управляемая библиотека) или [**рекогнитионресулт**](inkedit-recognitionresult.md) (только автоматизация) в потоке пользовательского интерфейса.
-   Методы [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) и [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) объекта [**Рекогнизерконтекст**](inkrecognizercontext-class.md) вызывают события [**распознавания**](inkrecognizercontext-recognition.md) и [**рекогнитионвисалтернатес**](inkrecognizercontext-recognitionwithalternates.md) в потоке распознавания фона.

### <a name="pen-input-panel-events"></a>События панели ввода пера

События [**пенинпутпанел**](peninputpanel-class.md) вызываются в потоке, в котором создается объект **пенинпутпанел** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Microsoft. Ink. InkCollector. Динамикрендеринг](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. Динамикрендеринг](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. Динамикрендеринг](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft. Ink. InkCollector. Ауторедрав](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. Ауторедрав](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. Ауторедрав](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

