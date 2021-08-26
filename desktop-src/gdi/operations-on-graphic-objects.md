---
description: После того как приложение создаст монитор или контроллер домена, он может начать рисовать на связанном устройстве или, в случае с КОНТРОЛЛЕРом памяти, он может начать рисование на точечном рисунке, хранящемся в памяти.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Операции с графическими объектами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ae7467e04f53196c839b6daa72482ab73845c3185208eb3cb886cb0ce6a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965624"
---
# <a name="operations-on-graphic-objects"></a>Операции с графическими объектами

После того как приложение создаст монитор или контроллер домена, он может начать рисовать на связанном устройстве или, в случае с КОНТРОЛЛЕРом памяти, он может начать рисование на точечном рисунке, хранящемся в памяти. Однако перед началом рисования и иногда во время прорисовки часто требуется заменить объекты по умолчанию новыми объектами.

Приложение может проверить атрибуты объекта по умолчанию, вызвав функции [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) и [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . Функция **жеткуррентобжект** возвращает дескриптор, идентифицирующий текущее перо, кисть, палитру, точечный рисунок или шрифт, а функция **GetObject** Инициализирует структуру, содержащую атрибуты этого объекта.

Некоторые принтеры предоставляют резидентные перья, кисти и шрифты, которые можно использовать для повышения скорости рисования в приложении. Для перечисления этих объектов можно использовать две функции: [**енумобжектс**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) и [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa). Если приложение должно перечислить резидентные перья или кисти, оно может вызвать функцию **енумобжектс** для проверки соответствующих атрибутов. Если приложение должно перечислять резидентные шрифты, оно может вызвать функцию **EnumFontFamilies** (которая также может перечислять шрифты GDI).

Когда приложение определит, что объекту по умолчанию требуется замена, он создает новый объект, вызывая одну из следующих функций создания.



| Графический объект | Функция                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**Креатебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**креатебитмапиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap), [**креатедискардаблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap), [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Brush          | [**Креатебрушиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect), [**креатедибпаттернбруш**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush), [**креатедибпаттернбрушпт**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt), [**креатехатчбруш**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush), [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush), [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Цветовая палитра  | [**креатепалетте**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Шрифт           | [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta), [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Перо            | [**Креатепен**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**креатепениндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Регион         | [**Креатиллиптикргн**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**креатиллиптикргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect), [**креатеполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**креатеполиполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn), [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Каждая из этих функций возвращает маркер, идентифицирующий новый объект. После того как приложение получит маркер, оно должно вызвать функцию [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) для замены объекта по умолчанию. Однако приложение должно сохранить маркер, идентифицирующий объект по умолчанию, и использовать этот маркер для замены нового объекта, если он больше не нужен. Когда приложение завершает рисование с помощью нового объекта, оно должно восстановить объект по умолчанию, вызвав функцию **SelectObject** , а затем удалить новый объект, вызвав функцию [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) . Невозможность удаления объектов вызывает серьезные проблемы с производительностью.

 

 



