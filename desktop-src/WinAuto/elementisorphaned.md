---
title: елементисорфанед
description: елементисорфанед
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf30478d7ca68f823cd3d87158f92af71ae1afb14bf8d17295eedee2b4a144d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829378"
---
# <a name="elementisorphaned"></a>елементисорфанед

## <a name="text"></a>Текст

Элемент является потерянным IAccessible в дереве

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Адресом интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта, полученного для заданных координат, является ссылка на потерянный элемент в дереве элементов.

Эта проблема возникает для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, поскольку элементы будут рассматриваться как невидимые и не будут объявлены пользователю.

## <a name="possible-causes"></a>Возможные причины

-   Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.
-   Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Навигация с помощью проверки попадания и расположения на экране](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




