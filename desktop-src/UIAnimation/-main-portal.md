---
title: Диспетчер анимации Windows
description: Диспетчер анимации Windows (Windows Animation) включает насыщенную анимацию элементов пользовательского интерфейса.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Анимация Windows анимации Windows, портал
- Анимация Windows для диспетчера анимации Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987632"
---
# <a name="windows-animation-manager"></a>Диспетчер анимации Windows

## <a name="purpose"></a>Назначение

Диспетчер анимации Windows (Windows Animation) включает насыщенную анимацию элементов пользовательского интерфейса. Он предназначен для упрощения процесса добавления анимации в пользовательский интерфейс приложения и позволяет разработчикам реализовывать анимации, которые являются гладкими, естественными и интерактивными.

Платформа анимации управляет планированием и выполнением анимаций. Он предоставляет библиотеку полезных математических функций для указания поведения элемента пользовательского интерфейса с течением времени, а также позволяет разработчикам реализовывать пользовательские функции, предоставляющие дополнительные поведений.

Анимация Windows не выполняет отрисовку; его можно использовать с любой графической платформой, включая Direct2D, Direct3D или GDI+.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                   | Описание                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Руководством по разработке анимации Windows](windows-animation-developer-guide.md)<br/> | В руководстве для разработчиков представлен обзор анимации Windows и приведен пример кода, охватывающего основные задачи анимации.<br/>          |
| [Справочник по анимации Windows](windows-animation-reference.md)<br/>               | Разделы, содержащиеся в этом разделе, содержат справочные спецификации для диспетчера анимации Windows.<br/>                           |
| [Примеры анимации Windows](windows-animation-samples.md)<br/>                   | Разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по диспетчеру анимации Windows. <br/> |
| [Глоссарий анимации Windows](-ui-animation-glossary.md)<br/>                     | В этом глоссарии содержатся термины и акронимы, представляющие интерес для разработчиков, использующих диспетчер анимации Windows.<br/>                               |



 

## <a name="developer-audience"></a>Аудитория разработчиков

Анимация Windows предназначена для использования опытными разработчиками на C/C++, знакомыми с COM, концепциями программирования пользовательского интерфейса и общими концепциями анимации.

## <a name="run-time-requirements"></a>Требования к среде выполнения

Диспетчер анимации Windows появился в Windows 7.

Приложения, для которых требуется поддержка Windows Animation Manager в Windows Vista, могут использовать обновление платформы для Windows Vista. Приложения, для которых требуется обновление платформы для Windows Vista, могут иметь Центр обновления Windows убедиться, что они установлены, или скачать и установить его в фоновом режиме. Дополнительные сведения см. в [статье об обновлении платформы для Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

-   [Общие сведения об анимации Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (видео)
-   [В Windows 7: подробный обзор и учебник по диспетчеру анимации](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (видео)
-   [Анимация Windows — дополнительные разделы](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (видео)
-   [Пример кода для диспетчера анимации Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>См. также

[Общие сведения об анимации (платформа .NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)