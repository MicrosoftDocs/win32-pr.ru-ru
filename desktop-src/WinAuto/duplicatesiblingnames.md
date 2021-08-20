---
title: дупликатесиблингнамес
description: дупликатесиблингнамес
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18f0e04ed0b2aba3b0637ca8535e2ca5a18110ee29edb397fc250944035f895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115334"
---
# <a name="duplicatesiblingnames"></a>дупликатесиблингнамес

## <a name="text"></a>Текст

Дублирование имени и роли однорангового элемента \\ " {0} \\ " приведет к неоднозначности между элементами.

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Элемент имеет то же имя и роль или ControlType, что и другой элемент.

Эта проблема может вызвать путаницу, так как средства чтения с экрана будут читать один и тот же текст для всех элементов с одинаковыми именами и ролями или ControlType.

## <a name="possible-causes"></a>Возможные причины

-   Имя элемента содержит текст Role/ControlType.
-   Имя элемента или его родительский элемент не заданы или заданы неправильно.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> <dt>

[**UIA \_ намепропертид**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Иуиаутоматионелемент. Куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




