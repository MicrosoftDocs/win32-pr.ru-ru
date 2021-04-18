---
title: Встроенные компоненты HLSL для трассировки лучей в Direct3D 12
description: Следующие Шейдеры HLSL поддерживают конвейер Direct3D 12 райтраЦинг.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2e7cc7053705bd66b37d91f3ee06a6a1f249a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710095"
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

## <a name="related-topics"></a>См. также

* [Справочник по основным](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
