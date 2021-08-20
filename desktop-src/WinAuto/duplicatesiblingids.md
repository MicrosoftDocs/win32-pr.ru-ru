---
title: дупликатесиблингидс
description: дупликатесиблингидс
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115361"
---
# <a name="duplicatesiblingids"></a>дупликатесиблингидс

## <a name="text"></a>Текст

Дублирующийся идентификатор автоматизации \\ " {0} \\ " приведет к неоднозначности между элементами.

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Элемент имеет тот же идентификатор автоматизации, что и другой элемент.

Эта проблема может вызвать проблемы с автоматизацией, препятствующие обращению кода теста к правильному элементу.

## <a name="possible-causes"></a>Возможные причины

-   Одноуровневые элементы имеют одинаковый идентификатор автоматизации.
-   Неверная реализация свойства UIA AutomationId.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**UIA \_ аутоматионидпропертид**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Иуиаутоматионелемент. Куррентаутоматионид**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




