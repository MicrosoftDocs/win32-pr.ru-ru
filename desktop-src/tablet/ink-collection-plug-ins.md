---
description: Объект RealTimeStylus изначально не выполняет накопления рукописного ввода. Чтобы использовать объект RealTimeStylus для сбора рукописных данных, создайте подключаемый модуль сборщика рукописных данных.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Подключаемые модули Ink-Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896866"
---
# <a name="ink-collection-plug-ins"></a>Подключаемые модули Ink-Collection

Объект [**RealTimeStylus**](realtimestylus-class.md) изначально не выполняет накопления рукописного ввода. Чтобы использовать объект **RealTimeStylus** для сбора рукописных данных, создайте подключаемый модуль сборщика рукописных данных.

Ниже приведен минимальный сценарий использования объекта [**RealTimeStylus**](realtimestylus-class.md) в форме, собирающей рукописный ввод.

1.  Создайте форму, реализующую интерфейс [**истилусасинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Создайте объект [**RealTimeStylus**](realtimestylus-class.md) и присоедините его к элементу управления в форме.
3.  Задайте интерес в уведомлениях Стилусдовн, пакеты и Стилусуп [в свойстве](/previous-versions/ms574886(v=vs.100)) объекта.
4.  В методах [**стилусдовн**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**пакетов**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)и [**стилусуп**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) формы добавьте код для управления уведомлениями о нажатии пера, пакетами и отправкой пера, которые отправляются из объекта [**RealTimeStylus**](realtimestylus-class.md) формы. Этот код должен хранить данные пера, а также создавать и сохранять штрихи.

Пример такого приложения см. в примере образца [рукописного сбора данных RealTimeStylus](realtimestylus-ink-collection-sample.md) .

> [!Note]  
> При возникновении события [дисплайсеттингсчанжед](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) вызовите метод [**модифидравингаттрибутес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) собранных штрихов в обработчике событий дисплайсеттингсчанжед для повторного вычисления свойств [Width](/previous-versions/ms582112(v=vs.100)) и [Height](/previous-versions/ms582106(v=vs.100)) . Это необходимо для учета возможных точек на дюйм (DPI), которые являются результатом события Дисплайсеттингсчанжед.

 

## <a name="ink-collection-and-recognizers"></a>Сбор и Распознаватели рукописного ввода

Ни анализ рукописного текста, ни распознавание рукописного ввода не являются функцией объекта [**RealTimeStylus**](realtimestylus-class.md) . Когда подключаемый модуль сборщика рукописных данных собирает рукописный ввод или как вы хотите распознавать рукописный ввод, вы можете скопировать рукописный ввод в объект [рекогнизерконтекст](/previous-versions/ms552546(v=vs.100)) или [делитель](/previous-versions/ms583616(v=vs.100)) . Дополнительные сведения о распознавании и анализе рукописного ввода см. в разделе [о распознавании рукописного текста](about-handwriting-recognition.md) или [объекте разделителя](the-divider-object.md).

## <a name="static-rendering"></a>Статическая отрисовка

Чтобы подготовить рукописный ввод при сборе, присоедините объект [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) к объекту [**RealTimeStylus**](realtimestylus-class.md) . Чтобы отобразить рукописный ввод после сбора, используйте объект модуля [подготовки](/previous-versions/ms552630(v=vs.100)) отчетов для рисования штрихов в соответствующем объекте [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) . Дополнительные сведения об объекте DynamicRenderer см. в разделе [подключаемые модули динамического рендеринга](dynamic-renderer-plug-ins.md). Пример как статической, так и динамической отрисовки см. в разделе [образец рукописного сбора данных RealTimeStylus](realtimestylus-ink-collection-sample.md).

 

 
