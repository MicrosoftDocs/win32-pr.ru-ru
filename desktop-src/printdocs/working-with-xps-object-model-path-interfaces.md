---
description: В этом разделе описывается, как использовать интерфейсы API документов XPS в модели XPS, связанные с путями.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Работа с интерфейсами Path в модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca66b65c6f20dc3b585de706e223df1f76d518a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545831"
---
# <a name="working-with-xps-om-path-interfaces"></a>Работа с интерфейсами Path в модели XPS

В этом разделе описывается, как использовать интерфейсы API документов XPS в модели XPS, связанные с путями.



| Имя интерфейса                                                            | Концептуальные дочерние элементы                                                                                                                                                                                                                                                                                                                                                                                                                                         | Описание                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Описывает графический элемент пути.<br/>                                                                                                                                                    |
| [**икспсомбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**икспсомтилебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**икспсомвисуалбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**икспсомимажебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**икспсомградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**икспсомлинеарградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**икспсомрадиалградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Кисть используется для заполнения области или линии.<br/>                                                                                                                                             |
| [**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Обеспечивает сплошные заливки или мазки цветом. <br/>                                                                                                                                                |
| [**икспсомвисуалбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Предоставляет визуальный объект, такой как путь, глиф или холст, или частичный визуальный элемент для использования в качестве заполнения или обводки мозаичного заполнения. <br/>                                                                  |
| [**икспсомимажебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Предоставляет изображение (или частичное изображение) для использования в качестве заливки или обводки мозаичного заполнения. <br/>                                                                                                           |
| [**икспсомлинеарградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Предоставляет линейный градиент, используемый в качестве заливки или обводки. <br/>                                                                                                                            |
| [**икспсомрадиалградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Предоставляет радиальный градиент, используемый в качестве заливки или обводки. <br/>                                                                                                                            |
| [**икспсомградиентстоп**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Определяет одну точку перегиба цветового значения в линейном или радиальном градиенте. <br/>                                                                                                     |
| [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Предоставляет определение области вектора, используемой в качестве области обрезки или определения пути. Состоит из одного или нескольких интерфейсов [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) . <br/> |
| [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Часть определения региона, на которую ссылается интерфейс [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) и состоящая из одного или нескольких сегментов. <br/>                                    |
| [**икспсомматрикстрансформ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | Нет<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Задает преобразование аффинного матрицы, применяемое к объекту во время отрисовки. <br/>                                                                                              |



 

## <a name="contents"></a>Содержимое

-   [OM-кисти XPS](xps-object-model-brushes.md)
-   [Градиенты модели XPS](xps-object-model-gradients.md)
-   [Геометрические объекты модели XPS](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Интерфейс Икспсомдашколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**Интерфейс Икспсомматрикстрансформ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




