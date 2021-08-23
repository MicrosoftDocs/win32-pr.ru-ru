---
description: Подключаемый модуль распознавателя — это объект, отслеживающий перемещение пера планшета для жестов, рукописного ввода или других объектов.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Подключаемые модули распознавателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b64f8f9b63cdbdc7309e7d9bd303ecce7a6b59b2e3b3c0cde976d1d6eefdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091533"
---
# <a name="recognizer-plug-ins"></a>Подключаемые модули распознавателя

Подключаемый модуль распознавателя — это объект, отслеживающий перемещение пера планшета для жестов, рукописного ввода или других объектов.

## <a name="system-gestures"></a>Системные жесты

Объект [**RealTimeStylus**](realtimestylus-class.md) распознает системные жесты. Объект **RealTimeStylus** добавляет объект [Системжестуредата](/previous-versions/ms824019(v=msdn.10)) в очередь [стилускуеуес](/previous-versions/ms824786(v=msdn.10)) в ответ на данные, завершающие жест, например объект [стилусупдата](/previous-versions/ms824057(v=msdn.10)) для [системжестуре](/previous-versions/bb345349(v=vs.100)). Дополнительные сведения см. в разделе [подключаемые данные и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>Объект GestureRecognizer

Объект [**GestureRecognizer**](gesturerecognizer-class.md) реализует интерфейсы [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) и [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Объект **GestureRecognizer** распознает жесты приложения. На внутреннем уровне объект **GestureRecognizer** использует для распознавания жестов средство распознавания жестов Майкрософт.

Когда объект [**GestureRecognizer**](gesturerecognizer-class.md) распознает жест, он добавляет пользовательские данные пера в очередь [стилускуеуес](/previous-versions/ms824786(v=msdn.10)) в ответ на объект [стилусупдата](/previous-versions/ms824057(v=msdn.10)) для Stroke. Свойству [кустомдатаид](/previous-versions/ms824748(v=msdn.10)) объекта [кустомстилусдата](/previous-versions/ms575208(v=vs.100)) присвоено значение [жестуререкогнитиондатагуид](/previous-versions/ms826344(v=msdn.10)) , а свойство [данных](/previous-versions/ms824749(v=msdn.10)) объекта кустомстилусдата содержит объект [жестуререкогнитиондата](/previous-versions/ms824594(v=msdn.10)) .

На следующей схеме показано, как объект [**GestureRecognizer**](gesturerecognizer-class.md) добавляет данные в данные пера планшета.

![Иллюстрация потока данных GestureRecognizer](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

На этой схеме круг с буквой SD представляет объект [стилусдовндата](/previous-versions/ms824107(v=msdn.10)) , а круг с буквой «P» представляют объекты [паккетсдата](/previous-versions/ms824590(v=msdn.10)) , которые уже были добавлены в очередь вывода объекта [**RealTimeStylus**](realtimestylus-class.md) и еще не были отправлены в асинхронную коллекцию подключаемых модулей. Кружок с буквой "SU" представляет объект [стилусупдата](/previous-versions/ms824057(v=msdn.10)) , который в настоящее время обрабатывается объектом **RealTimeStylus** . Он отправляется в коллекцию синхронных подключаемых модулей, а затем помещается в очередь вывода. Круговая буква «GR» представляет пользовательские данные пера, которые добавляются во входную очередь подключаемым модулем [**GestureRecognizer**](gesturerecognizer-class.md) в ответ на уведомление о создании пера, связанное с «SU». Пользовательское перо с буквой GR затем передается в синхронные подключаемые модули, а затем в выходную очередь до обработки следующих данных пера планшета. Пустой кружок представляет позицию в очереди вывода, в которой добавляются будущие данные пера планшета.

По умолчанию объект [**GestureRecognizer**](gesturerecognizer-class.md) распознает только жесты с одним росчерком; Однако объект **GestureRecognizer** можно задать для распознавания жестов с обводкой. Для жестов многоштриха объект [кустомстилусдата](/previous-versions/ms575208(v=vs.100)) добавляется в очередь [стилускуеуес](/previous-versions/ms824786(v=msdn.10)) в ответ на объект [стилусупдата](/previous-versions/ms824057(v=msdn.10)) для завершающего росчерка жеста. При распознавании жестов с обводкой вы можете получать уведомления для перекрывающихся наборов штрихов. Например, первый и второй штрихи могут располагаться как один жест, а второй росчерк сам по себе может быть распознан как жест. Дополнительные сведения о распознавании жестов для нескольких штрихов см. в разделе класс **GestureRecognizer** и свойство [максстрокекаунт](/previous-versions/ms826053(v=msdn.10)) .

Если вы используете объект [**GestureRecognizer**](gesturerecognizer-class.md) для распознавания жестов с помощью функции многоштриха, можно достичь оптимальной производительности, используя каскадную модель [**RealTimeStylus**](realtimestylus-class.md) и присоединив объект **GestureRecognizer** к дополнительному объекту **RealTimeStylus** . Дополнительные сведения о каскадной модели **RealTimeStylus** см. в статье [каскадная модель RealTimeStylus](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Особые рекомендации

В следующем списке приводятся другие моменты, которые следует учитывать при использовании объекта [**GestureRecognizer**](gesturerecognizer-class.md) .

-   Не следует присоединять объект [**GestureRecognizer**](gesturerecognizer-class.md) к более чем одному объекту [**RealTimeStylus**](realtimestylus-class.md) . После включения двух объектов **RealTimeStylus** , к которым присоединен объект **GestureRecognizer** , происходит следующее.
    -   Объект [**GestureRecognizer**](gesturerecognizer-class.md) создает исключение в ответ на второй вызов его метода реалтиместилусенаблед.
    -   Второй объект [**RealTimeStylus**](realtimestylus-class.md) , который был включен, создает объект [ErrorData](/previous-versions/ms824740(v=msdn.10)) и уведомляет остальные подключаемые модули в своих коллекциях подключаемых модулей ошибки.
    -   Объект [**GestureRecognizer**](gesturerecognizer-class.md) прекращает распознавание жестов.
-   Объект [**RealTimeStylus**](realtimestylus-class.md) создает исключение при вызове метода [аддкустомстилусдататокуеуе](/previous-versions/ms825761(v=msdn.10)) с параметром *GUID* , для которого задано значение глобального уникального идентификатора [Microsoft. стилусинпут. GestureRecognizer. жестуререкогнитиондатагуид](/previous-versions/ms826344(v=msdn.10)) .
-   Объект [**GestureRecognizer**](gesturerecognizer-class.md) реализуется как оболочка модели COM, и вы не можете напрямую вызывать методы интерфейса [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) или [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Дополнительные сведения о реализации COM и объекте [**RealTimeStylus**](realtimestylus-class.md) см. в разделе [Примечания по реализации для API-интерфейсов стилусинпут](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-gesture-recognition"></a>Распознавание пользовательских жестов

Вы можете создать настраиваемый подключаемый модуль распознавателя, распознающий рукописный ввод, жесты или другие объекты:

-   Передача сведений о штрихах в существующий объект [распознавателя](/previous-versions/ms829434(v=msdn.10)) и использование метода [аддкустомстилусдататокуеуе](/previous-versions/ms825761(v=msdn.10)) для добавления результатов в поток данных пера планшета.
-   Выполнение распознавания в подключаемом модуле и использование метода [аддкустомстилусдататокуеуе](/previous-versions/ms825761(v=msdn.10)) для добавления результатов в поток данных пера планшета.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Жесты приложения](application-gestures.md)
</dt> <dt>

[Системные жесты](system-gestures.md)
</dt> <dt>

[Временная шкала сообщений и системных событий мыши](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
