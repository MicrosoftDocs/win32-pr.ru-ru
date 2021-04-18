---
title: дупликатесиблингидс
description: дупликатесиблингидс
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700715"
---
# <a name="duplicatesiblingids"></a>дупликатесиблингидс

## <a name="text"></a>Текст

Дублирующийся идентификатор автоматизации \\ " {0} \\ " приведет к неоднозначности между элементами.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Элемент имеет тот же идентификатор автоматизации, что и другой элемент.

Эта проблема может вызвать проблемы с автоматизацией, препятствующие обращению кода теста к правильному элементу.

## <a name="possible-causes"></a>Возможные причины

-   Одноуровневые элементы имеют одинаковый идентификатор автоматизации.
-   Неверная реализация свойства UIA AutomationId.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**UIA \_ аутоматионидпропертид**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Иуиаутоматионелемент. Куррентаутоматионид**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




