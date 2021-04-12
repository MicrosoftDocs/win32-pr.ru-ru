---
description: Предоставляет доступ к событиям пера, поступающим от пера или сенсорных дигитайзеров.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Ссылка RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265452"
---
# <a name="realtimestylus-reference"></a>Ссылка RealTimeStylus

Предоставляет доступ к событиям пера, поступающим от пера или сенсорных дигитайзеров.

## <a name="in-this-section"></a>в этом разделе

-   [Классы и интерфейсы RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Перечисления RealTimeStylus](realtimestylus-enumerations.md)
-   [Структуры RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Комментарии

Этот объект реализует COM-интерфейс [**иреалтиместилус**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

Можно полностью управлять, динамически подготавливать, изменять и даже удалять данные из потока пакетов в синхронных и асинхронных подключаемых модулях объекта [**класса RealTimeStylus**](realtimestylus-class.md) .

Перо в реальном времени предоставляет способ создания объекта **инкколлектинг** , который является однопотоковым и резидентным в ПОТОКЕ пользовательского интерфейса приложения. Этот объект **инкколлектинг** получает доступ к данным пера в реальном времени из очереди. Объект **инкколлектинг** в сочетании с пером в режиме реального времени позволяет изменять выбор в режиме реального времени и изменять собранные данные рукописного ввода в режиме реального времени. Дополнительные сведения см. в разделе [доступ к вводу пера и управление](accessing-and-manipulating-stylus-input.md)им.

Используйте объект [**класса RealTimeStylus**](realtimestylus-class.md) , чтобы напрямую взаимодействовать с потоком данных пера планшета или блокировать рукописный ввод в режиме реального времени. Используйте объект [**класса InkCollector**](inkcollector-class.md) , объект [**класса InkOverlay**](inkoverlay-class.md) , элемент управления [InkPicture](inkpicture-control-reference.md) или элемент управления [InkEdit](inkedit-control-reference.md) , если поведение этих объектов по умолчанию обеспечивает необходимое поведение.

События пера в реальном времени находятся в определенном обработчике окна в пределах определенного прямоугольника ввода окна. Реалтиместилуссервице может передавать данные пера в несколько объектов [**класса RealTimeStylus**](realtimestylus-class.md) . Каждый объект **класса RealTimeStylus** получает данные пера для определенного раздела окна на основе определенного [**Свойства Иреалтиместилус:: виндовинпутректангле**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) для этого объекта **класса RealTimeStylus** . Объект **класса RealTimeStylus** получает данные пера, а затем обрабатывает его через список синхронных и асинхронных подключаемых модулей.

Разница между синхронными подключаемыми модулями и асинхронными подключаемыми модулями заключается в потоке, в котором они выполняются, и в вызывающей последовательности. Синхронные подключаемые модули вызываются потоком, в котором выполняется объект [**класса RealTimeStylus**](realtimestylus-class.md) . Каждый раз при создании экземпляра объекта **класса RealTimeStylus** создается экземпляр потока выполнения. Синхронные подключаемые модули выполняются в этом новом потоке, созданном для экземпляра объекта **класса RealTimeStylus** . Асинхронные подключаемые модули вызываются через пользовательский интерфейс или поток приложения после обработки потока пакетов синхронными подключаемыми модулями и хранятся в очереди вывода.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Идинамикрендерер**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**иреалтиместилус**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
