---
title: Печать и списки команд
description: Элемент управления печатью Direct2D \ 32; является новым компонентом в модуле Direct2D в Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0026071ce8e78fc2ea946e0fffff2993e32ab48a2a20d4de6cdb12ca9b1eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075056"
---
# <a name="printing-and-command-lists"></a>Печать и списки команд

[**Элемент управления печатью**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) [Direct2D](./direct2d-portal.md) — это новый компонент в модуле Direct2D в Windows 8. Этот компонент позволяет Direct2D приложениям повторно использовать вызовы рисования Direct2D (с точки зрения изменений состояния и примитивов отрисовки) для доставки результатов печати, сходных с отображаемыми на экране.

Интерфейс [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) представляет собой виртуальное задание печати. можно создать элемент управления печатью [Direct2D](./direct2d-portal.md) , чтобы запустить новое задание печати, передать содержимое Direct2D для каждой страницы, которую нужно напечатать, а затем закрыть элемент управления печатью для завершения задания печати.

> [!Note]  
> Элемент управления печатью сопоставляется с одним и тем же заданием печати, и его нельзя использовать повторно.

Элемент управления печатью [Direct2D](./direct2d-portal.md) преобразует и оптимизирует переданное содержимое Direct2D для подсистемы печати, которая работает с реальными принтерами для доставки фактической печати. Все сведения, относящиеся к печати, скрыты от приложений Direct2D. Это означает, что Direct2D приложения могут печататься, не зная, на каких устройствах они рисуются, или о переводе документов для печати.

Для печати с помощью [Direct2D](./direct2d-portal.md)необходимо подготовить один список команд Direct2D для каждой страницы, которую нужно напечатать, а затем передать этот список команд в элемент управления печатью Direct2D. Чтобы подготовить этот список команд Direct2D, просто создайте и настройте список команд в качестве целевого объекта для текущего контекста устройства, а затем нарисуйте его в контексте устройства точно так же, как при рисовании в точечный рисунок для отображения. Дополнительные сведения об устройствах и целевых объектах см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md) .

На схеме здесь показано взаимодействие между приложением, контекстом устройства, целевым объектом точечного рисунка, целевым объектом списка команд и элементом управления печатью.

> [!Note]  
> Windows печати Sub-System и компонентов принтера отображаются серым цветом, так как они полностью скрыты от приложений [Direct2D](./direct2d-portal.md) .

![Схема, показывающая, как коммандлист и печать взаимодействуют с приложением и Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Пример

Полный процесс печати содержимого Direct2D включает следующие шаги.

1.  Создайте элемент управления печатью для запуска задания печати.
2.  Добавьте страницу в элемент управления печатью, передав список команд.
3.  Повторите шаг 2 для каждой страницы в оставшейся части документа.
4.  Закройте элемент управления печатью, чтобы завершить задание печати.

Ниже приведен пример кода, демонстрирующий процесс.

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>Связанные темы

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[Повышение производительности приложений Direct2D и печати](improving-direct2d-performance.md)