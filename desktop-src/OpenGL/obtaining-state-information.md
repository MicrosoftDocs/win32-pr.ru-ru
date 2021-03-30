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
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775254"
---
# <a name="obtaining-state-information"></a>Получение сведений о состоянии

OpenGL поддерживает множество переменных состояния, влияющих на поведение многих функций. Некоторые из этих переменных имеют специализированные функции запросов.



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**глжетклипплане**](glgetclipplane.md) | [**глжетпикселмап**](glgetpixelmap.md)             | [**глжеттексимаже**](glgetteximage.md)                   |
| [**глжетлигхт**](glgetlight.md)         | [**глжетполигонстиппле**](glgetpolygonstipple.md) | [**глжеттекслевелпараметер**](glgettexlevelparameter.md) |
| [**глжетмап**](glgetmap.md)             | [**глжеттексенв**](glgettexenv.md)                 | [**глжеттекспараметер**](glgettexparameter.md)           |
| [**глжетматериал**](glgetmaterial.md)   | [**глжеттексжен**](glgettexgen.md)                 |                                                          |



 

Чтобы получить значения других переменных состояния, используйте [**глжетбулеанв**](glgetbooleanv.md), [**глжетдаублев**](glgetdoublev.md), [**глжетфлоатв**](glgetfloatv.md)или [**глжетинтежерв**](glgetintegerv.md), если это уместно. Сведения об использовании этих функций см. в разделе [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Другие функции запросов, которые вы можете использовать, — [**глжетеррор**](glgeterror.md), [**глжетстринг**](glgetstring.md)и [**глисенаблед**](glisenabled.md). (Дополнительные сведения о функциях, связанных с обработкой ошибок, см. в разделе [Обработка ошибок](handling-errors.md) .) Чтобы сохранить и восстановить наборы переменных состояния, используйте [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md).

-   [Использование функций запросов](using-the-query-functions.md)
-   [Обработка ошибок](error-handling.md)
-   [Коды ошибок OpenGL](opengl-error-codes.md)
-   [Сохранение и восстановление наборов переменных состояния](saving-and-restoring-sets-of-state-variables.md)
-   [Переменные состояния OpenGL](opengl-state-variables.md)
-   [Справочник по сведениям о состоянии](state-information-reference.md)

 

 




