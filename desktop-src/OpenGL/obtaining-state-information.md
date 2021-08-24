---
title: Получение сведений о состоянии
description: Получение сведений о состоянии
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, сведения о состоянии
- OpenGL, переменные состояния
- сведения о состоянии OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d13719964412bf8b74b9d2f4ef58d5a153a56fc2f8d15a3d8788cef94762637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144166"
---
# <a name="obtaining-state-information"></a>Получение сведений о состоянии

OpenGL поддерживает множество переменных состояния, влияющих на поведение многих функций. Некоторые из этих переменных имеют специализированные функции запросов.

:::row:::
    :::column:::
        [**глжетклипплане**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**глжетпикселмап**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**глжеттексимаже**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**глжетлигхт**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**глжетполигонстиппле**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**глжеттекслевелпараметер**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**глжетмап**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**глжеттексенв**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**глжеттекспараметер**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**глжетматериал**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**глжеттексжен**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

Чтобы получить значения других переменных состояния, используйте [**глжетбулеанв**](glgetbooleanv.md), [**глжетдаублев**](glgetdoublev.md), [**глжетфлоатв**](glgetfloatv.md)или [**глжетинтежерв**](glgetintegerv.md), если это уместно. Сведения об использовании этих функций см. в разделе [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Другие функции запросов, которые вы можете использовать, — [**глжетеррор**](glgeterror.md), [**глжетстринг**](glgetstring.md)и [**глисенаблед**](glisenabled.md). (Дополнительные сведения о функциях, связанных с обработкой ошибок, см. в разделе [Обработка ошибок](handling-errors.md) .) Чтобы сохранить и восстановить наборы переменных состояния, используйте [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md).

-   [Использование функций запросов](using-the-query-functions.md)
-   [Обработка ошибок](error-handling.md)
-   [Коды ошибок OpenGL](opengl-error-codes.md)
-   [Сохранение и восстановление наборов переменных состояния](saving-and-restoring-sets-of-state-variables.md)
-   [Переменные состояния OpenGL](opengl-state-variables.md)
-   [Справочник по сведениям о состоянии](state-information-reference.md)

 

 




