---
description: Планшетный ПК включает технологию для взаимодействия с данными пера планшета при их сборе.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Доступ к вводу пера и управление им
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df56b690a8b7459f42e7d692e47dff4e9f1c00330e02cc0c912d7a3ca3dda02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452062"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Доступ к вводу пера и управление им

Планшетный ПК включает технологию для взаимодействия с данными пера планшета при их сборе. Класс [**RealTimeStylus**](realtimestylus-class.md) является частью стилусинпут прикладных программных интерфейсов (API), которые обеспечивают доступ к потоку данных пера планшета. Эти интерфейсы API позволяют записывать, прерывать и изменять поток независимо от подготовки к просмотру и сбору рукописных данных.

API-интерфейсы Стилусинпут предназначены для:

-   Предоставление доступа в режиме реального времени к потоку данных пера планшета.
-   Обеспечьте потоку ПОЛЬЗОВАТЕЛЬСКОГО интерфейса блокировку динамической отрисовки рукописных данных, поставляя в очередь данные пакетов в потоке пользовательского интерфейса и делая коллекции рукописного ввода одиночными потоками.
-   Повышение производительности и снижение общего использования потоков при использовании объекта [**InkCollector**](inkcollector-class.md) , объекта [**InkOverlay**](inkoverlay-class.md) , элемента управления [InkPicture](inkpicture-control-reference.md) или элемента управления [InkEdit](inkedit-control-reference.md) для накопления рукописного ввода.

API-интерфейсы Стилусинпут не предназначены для работы с объектом [**InkCollector**](inkcollector-class.md) , объектом [**InkOverlay**](inkoverlay-class.md) , элементом управления [InkPicture](inkpicture-control-reference.md) или [InkEdit](inkedit-control-reference.md) .

Если необходимо напрямую взаимодействовать с потоком данных пера планшета или когда приложение может блокировать рукописный ввод в режиме реального времени, используйте объект [**RealTimeStylus**](realtimestylus-class.md) . Используйте объект [**InkCollector**](inkcollector-class.md) , объект [**InkOverlay**](inkoverlay-class.md) , элемент управления [InkPicture](inkpicture-control-reference.md) или элемент управления [InkEdit](inkedit-control-reference.md) , если поведение этих объектов по умолчанию обеспечивает необходимое поведение.

## <a name="in-this-section"></a>В этом разделе

В следующих разделах описываются элементы API-интерфейсов Стилусинпут:

-   [Архитектура API-интерфейсов Стилусинпут](architecture-of-the-stylusinput-apis.md)
-   [Работа с API-интерфейсами Стилусинпут](working-with-the-stylusinput-apis.md)
    -   [Работа с классом RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Подключаемые модули и класс RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Данные подключаемого модуля и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Примечания по реализации для API-интерфейсов Стилусинпут](implementation-notes-for-the-stylusinput-apis.md)
    -   [Подключаемые модули сбора рукописных данных](ink-collection-plug-ins.md)
    -   [Подключаемые модули динамического рендеринга](dynamic-renderer-plug-ins.md)
    -   [Подключаемые модули распознавателя](recognizer-plug-ins.md)
-   [Рекомендации по использованию API-интерфейсов Стилусинпут](considerations-when-using-the-stylusinput-apis.md)
    -   [Рекомендации по проектированию для API-интерфейсов Стилусинпут](design-considerations-for-the-stylusinput-apis.md)
    -   [Рекомендации по потокам для API-интерфейсов Стилусинпут](threading-considerations-for-the-stylusinput-apis.md)

[Модель каскадного RealTimeStylus](the-cascaded-realtimestylus-model.md)

-   [Рекомендации по обработке ошибок для API-интерфейсов Стилусинпут](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Рекомендации по повышению производительности для API-интерфейсов Стилусинпут](performance-considerations-for-the-stylusinput-apis.md)
-   [Рекомендации по частичному доверию для API-интерфейсов Стилусинпут](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Пример подключаемого модуля RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Пример коллекции рукописных данных RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



