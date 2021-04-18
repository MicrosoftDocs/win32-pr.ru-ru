---
title: елементисорфанед
description: елементисорфанед
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700711"
---
# <a name="elementisorphaned"></a>елементисорфанед

## <a name="text"></a>Текст

Элемент является потерянным IAccessible в дереве

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Адресом интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта, полученного для заданных координат, является ссылка на потерянный элемент в дереве элементов.

Эта проблема возникает для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, поскольку элементы будут рассматриваться как невидимые и не будут объявлены пользователю.

## <a name="possible-causes"></a>Возможные причины

-   Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.
-   Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Навигация с помощью проверки попадания и расположения на экране](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




