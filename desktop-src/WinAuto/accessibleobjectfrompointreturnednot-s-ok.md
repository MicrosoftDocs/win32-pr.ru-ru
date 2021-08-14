---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: Акцессиблеобжектфромпоинтретурнеднот \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ceabd15e5a401bb67ac14af5a7fb83b96543b4b8046ceee2349d8d57b8de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327690"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Навигация с помощью проверки попадания и расположения на экране](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




