---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: Акцессиблеобжектфромпоинтретурнеднот \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85756504520f7d665c1cd1ba7db7c76c1ec5b12a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330171"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>Акцессиблеобжектфромпоинтретурнеднот \_ S \_ OK

## <a name="text"></a>Текст

Акцессиблеобжектфромпоинт ( {0} , {1} ) возвращается {2} и ожидается S \_ ОК

## <a name="type"></a>Тип

Предупреждение

## <a name="description"></a>Описание

[**Акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) не вернул значение S \_ ОК, как ожидалось для заданных координат.

## <a name="possible-causes"></a>Возможные причины

-   Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.
-   Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Навигация с помощью проверки попадания и расположения на экране](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




