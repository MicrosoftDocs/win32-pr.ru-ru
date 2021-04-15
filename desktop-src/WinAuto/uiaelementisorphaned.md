---
title: уиаелементисорфанед
description: уиаелементисорфанед
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710093"
---
# <a name="uiaelementisorphaned"></a>уиаелементисорфанед

## <a name="text"></a>Текст

Элемент является потерянным элементом AutomationElement в дереве

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Адрес интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) объекта, полученного для заданных координат, является ссылкой на потерянный элемент в дереве элементов.

Эта проблема возникает для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, поскольку элементы будут рассматриваться как невидимые и не будут объявлены пользователю.

## <a name="possible-causes"></a>Возможные причины

-   Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.
-   Неправильная или недопустимая реализация модели автоматизации пользовательского интерфейса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Иуиаутоматионелемент. Елементфромпоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




