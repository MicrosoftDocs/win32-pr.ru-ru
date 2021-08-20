---
title: Для элементов Драгпаттерн/Драгдроппаттерн требуется допустимый Дропеффект
description: Для элементов Драгпаттерн/Драгдроппаттерн требуется допустимый Дропеффект
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115682"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Для элементов Драгпаттерн/Драгдроппаттерн требуется допустимый Дропеффект

## <a name="text"></a>Текст

Элементы, поддерживающие перетаскивание, должны иметь допустимый набор "Дропеффект"

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Элемент поддерживает либо [**иуиаутоматиондрагпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) , либо [**иуиаутоматиондроптаржетпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), но не имеет допустимого набора свойств [**дропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) .

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана. Пользователь не сможет определить, какое действие этот объект имеет при перетаскивании.

## <a name="possible-causes"></a>Возможные причины

-   Элемент или его родитель не создал [**дропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) или [**дропеффектс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) неправильно назначенное имя или метка.
-   Разработчик не знает, что читатели экрана читают Дропеффект.

 

 




