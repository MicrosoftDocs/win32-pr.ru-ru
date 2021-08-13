---
title: Интерфейсы перехода
description: в этом разделе содержатся справочные спецификации для интерфейсов диспетчера анимации Windows, поддерживающих переходы.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418604"
---
# <a name="transition-interfaces"></a>Интерфейсы перехода

в этом разделе содержатся справочные спецификации для интерфейсов диспетчера анимации Windows, поддерживающих переходы.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                     | Описание                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иуианиматионинтерполатор**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Определяет методы для создания пользовательского интерполяции.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Расширяет интерфейс [**иуианиматионинтерполатор**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) , определяющий методы для создания пользовательского интерполяции. [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) поддерживает интерполяцию в заданном измерении. <br/>        |
| [**иуианиматионпримитивеинтерполатион**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Определяет метод, позволяющий пользовательскому интерполяции предоставлять сведения о переходах в виде кривой с эффектом полинома, к которому выполняется анимация.<br/>                                                                                                        |
| [**иуианиматионтранситион**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Определяет переход, который определяет, как изменяется переменная анимации со временем.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Расширяет интерфейс [**иуианиматионтранситион**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) , определяющий переход. Переход [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) определяет, как изменяется переменная анимации с течением времени в заданном измерении.<br/> |
| [**иуианиматионтранситионфактори**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Определяет метод для создания переходов из пользовательских интерполяций.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Определяет метод для создания переходов из пользовательских интерполяций.<br/>                                                                                                                                                                                            |
| [**иуианиматионтранситионлибрари**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Определяет библиотеку стандартных переходов. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Определяет библиотеку стандартных переходов для указанного измерения.<br/>                                                                                                                                                                                            |
| [**иуианиматионвариабле**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Определяет переменную анимации, которая представляет визуальный элемент, который может быть анимирован.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Определяет переменную анимации, которая представляет визуальный элемент, который может быть анимирован в нескольких измерениях.<br/>                                                                                                                                                   |
| [**иуианиматионвариаблечанжехандлер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Определяет метод для обработки событий, связанных с обновлением переменных анимации.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Определяет метод для обработки событий обновления переменной анимации. [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) обрабатывает события, происходящие в указанном измерении.<br/>                                                            |
| [**иуианиматионвариаблеинтежерчанжехандлер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Определяет метод для обработки событий обновления переменной анимации.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Определяет метод для обработки событий обновления переменной анимации. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) обрабатывает события, происходящие в указанном измерении.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Определяет метод обработки событий обновления кривой анимации. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы](windows-animation-reference.md)
</dt> </dl>

 

 





