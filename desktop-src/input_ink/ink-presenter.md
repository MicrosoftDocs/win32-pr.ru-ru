---
description: API-интерфейсы обработчика рукописного ввода позволяют классическим приложениям Майкрософт Win32 управлять вводом, обработкой и отрисовкой рукописного ввода (стандартного и модифицированного) с помощью объекта InkPresenter, добавляемого в визуальное дерево приложения DirectComposition.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Показ рукописных данных
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265517"
---
# <a name="ink-presenter"></a>Показ рукописных данных

Интерфейсы API-интерфейсов рукописного ввода позволяют приложениям Microsoft Win32 управлять вводом, обработкой и отрисовкой рукописного ввода (Standard и Modified) с помощью объекта [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) , вставленного в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения.

> [!Note]
>
> Стандартный ввод рукописных данных (кончик пера или кончик или кнопка ластика) не изменен с помощью вторичного уровня доступности, такого как кнопка с изображением пера, правая кнопка мыши или аналогичный.

Приложения универсальная платформа Windows (UWP), использующие XAML (XAML), предоставляют эту функцию с помощью элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) , а также объекта [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) , который подключается к визуальному дереву XAML [DirectComposition](../directcomp/directcomposition-portal.md) . Дополнительные сведения см. в разделе [взаимодействие пером и](/windows/uwp/design/input/pen-and-stylus-interactions)пера.

Модуль [подготовки рукописного ввода](ink-renderer.md) предназначен для использования разработчиками универсальных приложений Windows, заинтересованными в предоставлении функциональных возможностей элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)на основе XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) в собственных приложениях Win32.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                               | Описание                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Классы для рукописного показа](ink-presenter-classes.md)<br/>       | Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для классов в области рукописного ввода. <br/>    |
| [Интерфейсы выступающих чернил](ink-presenter-interfaces.md)<br/> | Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для интерфейсов для показа рукописных данных. <br/> |



 

## <a name="related-topics"></a>См. также

Взаимодействие [рукописного ввода](ink-presenter.md), [перо и](/windows/uwp/design/input/pen-and-stylus-interactions)перо, [Пример анализа рукописного текста](/samples/microsoft/windows-universal-samples/inkanalysis/), [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [сложный образец для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода
