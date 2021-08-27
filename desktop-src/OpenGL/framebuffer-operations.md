---
title: Операции буфера кадров
description: Чтобы выбрать буфер, в который записываются значения цветов, используйте Глдравбуффер.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Конвейер обработки OpenGL, операции буфера кадров
- фрамебуфферс, операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082334"
---
# <a name="framebuffer-operations"></a>Операции буфера кадров

Чтобы выбрать буфер, в который записываются значения цветов, используйте [**глдравбуффер**](gldrawbuffer.md). Вы используете четыре различные функции для маскирования записи битов на каждый из логических фрамебуфферс после выполнения всех операций по каждому фрагменту:

-   [**глиндексмаск**](glindexmask.md)
-   [**глколормаск**](glcolormask.md)
-   [**глдепсмаск**](gldepthmask.md)
-   [**глстенЦилмаск**](glstencilmask.md)

Функция [**Глаккум**](glaccum.md) управляет операцией буфера накопления. Наконец, [**глклеар**](glclear.md) устанавливает каждый пиксель в заданном подмножестве буферов в значение, указанное в [**глклеарколор**](glclearcolor.md), [**глклеариндекс**](glclearindex.md), [**глклеардепс**](glcleardepth.md), [**глклеарстенЦил**](glclearstencil.md)или [**глклеараккум**](glclearaccum.md).

 

 




