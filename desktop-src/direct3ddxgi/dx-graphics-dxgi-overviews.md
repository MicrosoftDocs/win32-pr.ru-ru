---
description: Графическая инфраструктура Microsoft DirectX (DXGI) управляет задачами низкого уровня, которые могут быть независимыми от среды выполнения Direct3D Graphics. DXGI предоставляет общую платформу для нескольких версий Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Руководством по программированию для DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0ac41155557c14ca41f8e0ea9f1836247bd3b78da213c1fbbed521499eae7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518387"
---
# <a name="programming-guide-for-dxgi"></a>Руководством по программированию для DXGI

Графическая инфраструктура Microsoft DirectX (DXGI) управляет задачами низкого уровня, которые могут быть независимыми от среды выполнения Direct3D Graphics. DXGI предоставляет общую платформу для нескольких версий Direct3D.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                                              | Описание                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Общие сведения о DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | В этом разделе содержатся следующие подразделы.<br/>                                                                                                                   |
| [Усовершенствования DXGI 1,2](dxgi-1-2-improvements.md)<br/>                                                                      | В DXGI 1,2 добавлены следующие функциональные возможности.<br/>                                                                                                       |
| [Усовершенствования DXGI 1,3](dxgi-1-3-improvements.md)<br/>                                                                      | В DXGI 1,3 добавлена следующая функциональность, которая включается в Windows 8.1.<br/>                                                            |
| [Усовершенствования DXGI 1,4](dxgi-1-4-improvements.md)<br/>                                                                      | В DXGI 1,4 добавлены или изменены следующие функциональные возможности, в основном поддерживающие Direct3D 12. <br/>                                                           |
| [Усовершенствования DXGI 1,5](dxgi-1-5-improvements.md)<br/>                                                                      | В DXGI 1,5 добавлены следующие функциональные возможности для поддержки более гибкого указания и дублирования форматов выходных данных.<br/>                                |
| [Усовершенствования DXGI 1,6](dxgi-1-6-improvements.md)<br/>                                                                      | Для обнаружения HDR-отображений в DXGI 1,6 добавлены следующие функциональные возможности.<br/>                                                                       |
| [Использование DirectX с дисплеями с широким динамическим диапазоном и расширенным управлением цветами](../direct3darticles/high-dynamic-range.md)     | в этом разделе представлен технический обзор визуализации содержимого direct3d 11 и direct3d 12 с высоким динамическим диапазоном на HDR10 дисплеи с помощью Windows 10 расширенная поддержка цвета.<br/> |
| [Отображение частоты обновления переменных](variable-refresh-rate-displays.md)<br/>                                                    | Для отображения частоты обновления переменных требуется *разрыв* , так как он также называется «вертикальной синхронизации-Off».<br/>                                                    |
| [Использование гамма-коррекции](using-gamma-correction.md)<br/>                                                                    | Гамма-коррекция или гамма для краткости — это имя нелинейной операции, используемой системами для кодирования и дешифрования значений пикселей в изображениях.<br/>                        |
| [Поддержка формата для функции Direct3D 10Level9 9,1 Hardware](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10Level9 9,1.<br/>        |
| [Поддержка формата для функции Direct3D 10Level9 9,3 Hardware](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10Level9 9,3.<br/>        |
| [Поддержка формата для оборудования на уровне компонентов Direct3D 10,0](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10,0.<br/>                        |
| [Поддержка формата для оборудования на уровне компонентов Direct3D 10,1](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 10,1.<br/>                        |
| [Поддержка формата для оборудования на уровне компонентов Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 11,0.<br/>          |
| [Поддержка формата для оборудования на уровне компонентов Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 11,1.<br/>          |
| [Поддержка формата для оборудования на уровне компонентов Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)<br/>               | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании уровня функции Direct3D 12,0.<br/>          |
| [Поддержка формата для оборудования на уровне компонентов Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)<br/>               | В этом разделе указываются форматы (значения [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ), которые поддерживаются в оборудовании Direct3D 12,1.<br/>                        |
| [Проверка поддержки компонентов оборудования](checking-hardware-feature-support.md)<br/>                                              | В этом разделе описывается, как проверить поддержку формата для оборудования на уровне функций Direct3D с помощью вызовов API.<br/>                                                       |
| [Для достижения оптимальной производительности используйте модель перелистывания DXGI](for-best-performance--use-dxgi-flip-model.md)<br/>                              | В этом разделе содержатся рекомендации для разработчиков по повышению производительности и эффективности в стеке презентации на современных версиях Windows.<br/>                 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Ссылка на DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[Графическая инфраструктура DirectX (DXGI): рекомендации](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
