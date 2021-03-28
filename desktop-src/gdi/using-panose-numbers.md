---
description: Файлы шрифтов TrueType содержат номера PANOSE, которые могут использоваться приложениями для выбора шрифта, близко соответствующего его спецификациям.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Использование номеров PANOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266187"
---
# <a name="using-panose-numbers"></a>Использование номеров PANOSE

Файлы шрифтов TrueType содержат номера PANOSE, которые могут использоваться приложениями для выбора шрифта, близко соответствующего его спецификациям. Система PANOSE классифицирует лиц на 10 различных атрибутов. Дополнительные сведения об этих атрибутах см. в разделе [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose). Структура **Panose** является частью структуры [**аутлинетекстметрик**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (значения которой заполняются путем вызова функции [**жетаутлинетекстметрикс**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).

Атрибуты PANOSE оцениваются по отдельности на шкале. Результирующие значения объединяются для получения числа. Учитывая это число для шрифта и математическую метрику для измерения расстояний в PANOSE пространстве, приложение может определить соседних соседей.

 

 



