---
title: Для элементов Драгпаттерн/Драгдроппаттерн требуется имя
description: Для элементов Драгпаттерн/Драгдроппаттерн требуется имя
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700471"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>Для элементов Драгпаттерн/Драгдроппаттерн требуется имя

## <a name="text"></a>Текст

Элементы, поддерживающие перетаскивание, должны иметь допустимый набор "Name"

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Элемент поддерживает либо [**иуиаутоматиондрагпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) , либо [**иуиаутоматиондроптаржетпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), но не имеет допустимого набора имен.

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана. Пользователь не сможет определить, что этот объект с момента считывания с экрана не будет считать допустимое имя, чтобы отличать этот элемент от перетаскивания.

## <a name="possible-causes"></a>Возможные причины

-   Элемент или его родитель имеет неправильно назначенное имя или подпись.
-   Разработчик не знает, что читатели экрана считывают имена и типы элементов управления.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> <dt>

[**UIA \_ намепропертид**](uiauto-automation-element-propids.md)
</dt> <dt>

[**Иуиаутоматионелемент:: Куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




