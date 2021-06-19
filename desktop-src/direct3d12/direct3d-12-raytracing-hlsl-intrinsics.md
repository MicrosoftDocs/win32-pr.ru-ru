---
title: Встроенные компоненты HLSL для трассировки лучей в Direct3D 12
description: Просмотрите ссылки на статьи, описывающие встроенные функции языка шейдеров (HLSL), которые поддерживают конвейер Direct3D 12 райтраЦинг.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06687866354611f44f295ff4fe2cf171068e83c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396479"
---
# <a name="raytracing-hlsl-intrinsics"></a>Встроенные функции райтраЦинг HLSL

Следующие функции HLSL интриниск поддерживают конвейер райтраЦинг Direct3D 12. 

## <a name="in-this-section"></a>В этом разделе



| Раздел | Описание |
|-|-|
| [**Функция AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Используется в любом шейдере нажатия для фиксации текущего попадания, а затем для поиска большего числа попаданий для луча. |
| [**Функция CallShader**](callshader-function.md) | Вызывает другой шейдер из шейдера. |
| [**Функция IgnoreHit**](ignorehit-function.md) | Вызывается из любого шейдера нажатия, чтобы отклонить попадание и завершить шейдер. |
| [**Функция Примитивеиндекс**](primitiveindex.md) | Извлекает автоматически сформированный индекс примитива внутри геометрии внутри экземпляра структуры ускорения нижнего уровня. |
| [**Функция ReportHit**](reporthit-function.md) | Вызывается шейдером пересечения для сообщения пересечения лучей. |
| [**Функция TraceRay**](traceray-function.md) | Отправляет луч в поиск на предмет попаданий в структуре ускорения. |

## <a name="related-topics"></a>Связанные темы

* [Справочник по основным](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
