---
title: уианамеленгстулонг
description: уианамеленгстулонг
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- Идентификатор UIA_NamePropertyId AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411293"
---
# <a name="uianamelengthtoolong"></a>уианамеленгстулонг

## <a name="text"></a>Текст

Имя элемента не должно возвращать строку длиннее {0} символа

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Имя элемента содержит слишком много символов. Например, метод [**иуиаутоматионелемент:: куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) , используемый для получения имени UIA элемента, возвращает строку, превышающую ограничение.

Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет неправильно назначенное имя или подпись.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**UIA \_ намепропертид**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Иуиаутоматионелемент:: Куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




